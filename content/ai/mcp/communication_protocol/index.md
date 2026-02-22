---
title: "MCP Protocol"
description: "An overview of the MCP Protocol"
draft: true
ShowToc: true
TocOpen: true
author: "Gary Thomas"
date: 2025-05-28
tags: ["MCP", "JSON-RPC"]
category: "AI"

---

## Introduction

The MCP defines a standarised communication protocol that enables Clients and Servers to exchange consistent message content.

## JSON-RPC

At its core, MCP uses JSON-RPC 2.0 as the message format for all communication between Clients and Servers. JSON-RPC is a lightweight remote procedure call protocol encoded in JSON, which makes it:

- Human readable and easy to debug
- Language agnostic, supporting implementation in any programming environment
- Established standard with clear specificatgions and widespread adoption and support

![Messages](mcp-protocol-req-resp-notif.png)

### Request

The request is sent from **Client** to **Server** to initiate the start of an operation.

The Request message contains the following:
- A unique identifier (id)
- The method name to be called (e.g. tools/execute)
- The parameters to be passed to the method (e.g. tool_name, tool_args, these are optional)

The following is an example of a Request message:

```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "method": "tools/execute",
    "params": {
        "name": "weather",
        "args": {
            "location": "Sydney"
        }
    }
}
```

### Response

The response is sent from **Server** to **Client** to indicate the result of the operation.

The Response message contains the following:
- A unique identifier (id) corresponding to the identifier in the request
- either a **result** (success) or an **error** (failure)

The following is an example of a Response message:

```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": {
        "temperature": "22°C",
        "humidity": "80%",
        "conditions": "Sunny"
    }
}
```

The following is an example of a Response message with an error:

```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "error": {
        "code": -32601,
        "message": "Invalid location parameter"
    }
}
```

### Notification

The notification is sent from **Server** to **Client** to indicate an event has occurred or provide updates, and do not require a response. Note - The use of an identifier (id) is optional for notifications.

The Notification message contains the following:
- The method name to be called (e.g. tools/execute)
- The parameters indicating some status or data related to the event

The following is an example of a Notification message:

```json
{
    "jsonrpc": "2.0",
    "method": "progress",
    "params": {
        "message": "Processing...",
        "progress": 50
    }
}
```

## Transport

MCP is agnostic to the transport layer, and can be implemented over any transport layer that supports JSON-RPC 2.0. Two primary transports are supported:

- HTTP + SSE (Server-Sent Events)/Streamable HTTP
- stdio

### HTTP + SSE (Server-Sent Events)/Streamable HTTP

```markdown
> Clients and servers can maintain backwards compatibility with the **deprecated** HTTP+SSE transport (from protocol version 2024-11-05). Note Streamable HTTP is the current recommended transport and is compatible with the deprecated HTTP+SSE transport.
```

This transport is used for remote communication where the Client and Server may be running on different machines.

Communication happens over HTTP, with the Server using Server-Sent Events (SSE) to **push** updates to the client over a persistent connection.

The main Advantages of this transport are that it works across networks, enables integration with web services, and is compatible with serverless environments.

Recent updates to the MCP standard have introduced or refined “Streamable HTTP,” which offers more flexibility by allowing servers to dynamically upgrade to SSE for streaming when needed, while maintaining compatibility with serverless environments.

```markdown
> **Use Cases** for this transport are connecting to remote APIs, cloud services or shared services.
```

### stdio

This transport is used for local communication where the Client and Server are running on the same machine.

The **Host** launches the **Server** and as subprocesses. Communication happens over standard input and output (stdin and stdout), with the **Host** writing to stdin and reading from stdout.

The main advantage of this transport is that it is simple to implement and does not require any additional infrastructure or network configuration within security sandbox enforced by the operating system.

```markdown
> **Use Cases** for this transport are local tools like file system access or running local scripts
```

## Interaction Lifecycle

The MCP defines a structured interaction Lifecycle between **Client** and **Server**. The lifecycle is as follows:

### Initialisation

The Client connects to the Server and they exchange protocol versions and capabilities, and the Server responds with its supported protocol version and capabilities.
The Client confirms the completion of the initialisation by sending a notification to the Server.

![Initialisation](mcp-initialisation.png)

### Discovery

The Client requests information about the available capabilities of the Server. The Server responds with a list of available tools.
The interaction could be repeated for each tool, resource or prompt type.

![Discovery](mcp-discovery.png)

### Execution

The **Client** requests the execution of a tool, resource or prompt as required by the **Host**. The **Server** responds with the result of the execution. An intermediate Notification(s) may be sent from Server to Client to provide progress updates or other information prior to the response.

![Execution](mcp-execution.png)

### Termination

The interaction is terminated when the **Client** sends a notification to the **Server** to indicate that the interaction is complete and the **Server** acknowledges the termination request.
The **Client** sends a final exit notification to complete the termination after receiving the final response from the **Server**.

![Termination](mcp-termination.png)

## Protocol Evolution

The MCP is designed to be extensible and adaptable. The initialisation phase includes version negotiation, allowing for backwards compatibility as the protocol evolves. 
Capability discovery allows clients to adapt to the capabilities of the server, and the protocol can be extended to support new capabilities as they become available as well as allowing a mix of features in the same environment.