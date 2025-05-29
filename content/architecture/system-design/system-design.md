---
title: "System Design"
description: "Patterns and approaches to system design what are the trade-offs and also the patterns that can be used to address them"
summary: "Patterns and approaches to system design"
draft: true
tags: ["system-design", "patterns", "trade-offs"]
categories: ["architecture"]
author: "Gary Thomas"
date: 2025-05-09
---

## System Design

Designing distributed systems is both an art and a science — one that involves choosing the right patterns and trade-offs to meet scalability, reliability, and performance goals. In this post, we explore the foundational components of system design, common design patterns, and the architectural considerations that help address real-world challenges. Whether you're preparing for a system design interview or leading an architecture review, these building blocks provide a solid foundation.

### Characteristics of Distributed Systems

### Load Balancing

### Caching

### Data Partitioning

Data partitioning, also known as sharding, is a fundamental strategy for achieving horizontal scalability in distributed systems. It involves dividing data into distinct subsets and distributing them across multiple databases or storage nodes. Key considerations include:

#### Partitioning Strategies

- **Horizontal Partitioning (Sharding)**: Splits data rows across partitions, commonly by user ID or account number.
- **Vertical Partitioning**: Segregates data by columns, often used to isolate infrequently accessed data.
- **Functional Partitioning**: Divides data by functionality (e.g., customer vs. order data).
- **Directory-Based Partitioning**: Uses a lookup service to map data keys to specific partitions for flexibility.

#### Choosing a Partition Key

- Select keys that ensure even data distribution to prevent hotspots.
- Align the key with common query patterns to minimize cross-partition queries.
- Prefer immutable keys to avoid the complexity of data movement.

#### Avoiding Hotspots

- Hot partitions can degrade performance. Hash-based partitioning helps distribute data uniformly.
- Composite keys may help when single fields lead to uneven distribution.

#### Rebalancing and Resharding

- Plan for dynamic scaling. As data grows, partitions may need to be split or merged.
- Use consistent hashing to minimize data movement during rebalancing.

#### Data Locality and Query Efficiency

- Joins across partitions are expensive. Where possible, co-locate related data.
- Denormalization and materialized views can help mitigate cross-partition access costs.

#### Transactions Across Partitions

- Distributed transactions are complex and should be avoided where possible.
- Use local transactions within partitions, and consider saga patterns for operations that span partitions.

#### Operational Considerations

- Increased complexity in monitoring, backups, and failover management.
- Automation is key for partition creation, migration, and health checks.

#### Partition Size Management

- Enforce upper bounds on partition size to prevent any one partition from growing uncontrollably.
- Time-based partitioning is useful for log or event data to manage growth.

#### Fault Isolation

- Partitions can help contain failures to a subset of the data.
- Implement intra-partition replication to maintain high availability.

Data partitioning is not a one-time task; it requires ongoing monitoring and adaptation as access patterns, data volumes, and business needs evolve.

### Consistency Models and Trade-offs

In distributed systems, consistency models define the rules for how and when changes made by one component become visible to others. Choosing the right consistency model is essential for balancing correctness, availability, and performance.

#### Strong Consistency

- Guarantees that all reads return the most recent write.
- Suitable for scenarios where data correctness is critical (e.g., banking, inventory systems).
- Often incurs higher latency and coordination overhead.
- Implemented using consensus protocols (e.g., Paxos, Raft).

#### Eventual Consistency

- Guarantees that, in the absence of new updates, all nodes will eventually converge to the same value.
- Ideal for high-availability systems where temporary inconsistency is acceptable.
- Used in systems like DNS, shopping carts, and social feeds.

#### Causal Consistency

- Preserves the order of causally related operations.
- More intuitive than eventual consistency without the cost of strong consistency.
- Appropriate for collaborative tools or messaging platforms.

#### Read-Your-Writes Consistency

- Ensures that a user sees their own updates immediately.
- A weaker model that improves user experience while maintaining availability.

#### Trade-offs

- **Latency vs. Consistency**: Stronger consistency requires coordination, increasing latency.
- **Availability vs. Consistency**: CAP theorem states a system can only guarantee two of the three — Consistency, Availability, and Partition Tolerance. (See entries on CAP Theorem for more details)
- **Throughput vs. Consistency**: High throughput often necessitates looser consistency.
- **Developer Complexity**: Weaker consistency shifts responsibility to application logic to handle stale reads or retries.

Designers must choose the appropriate consistency model based on application needs, user expectations, and operational environment. It’s common to use a blend of models — for example, strong consistency for financial transactions and eventual consistency for audit logs or notifications.

#### Comparison Table of Consistency Models

| Model                    | Guarantees                                             | Latency   | Availability | Complexity | Typical Use Cases                             |
|--------------------------|--------------------------------------------------------|-----------|--------------|------------|-----------------------------------------------|
| Strong Consistency       | All reads return the most recent write                | High      | Lower        | High       | Banking, inventory, critical systems          |
| Eventual Consistency     | All nodes converge to the same value over time        | Low       | High         | Medium     | DNS, user feeds, shopping carts               |
| Causal Consistency       | Causally related operations maintain correct order     | Medium    | Medium       | Medium     | Collaborative tools, chat systems             |
| Read-Your-Writes         | Users immediately see their own updates               | Low       | High         | Low        | User dashboards, settings                     |

This table highlights how different consistency models balance correctness, latency, and availability, helping guide the selection based on system requirements.

### Proxies

### Redundancy

### Replication

### Data - NoSql, Sql and Other

### CAP Theorem

The CAP Theorem, formulated by Eric Brewer, states that a distributed system can only guarantee two out of the following three properties at any given time:

- **Consistency (C)**: Every read receives the most recent write.
- **Availability (A)**: Every request receives a response, even if it is not the most recent.
- **Partition Tolerance (P)**: The system continues to operate despite arbitrary network partitions.

According to the theorem, a system must trade off one of these when a partition occurs:
- **CP systems** sacrifice availability for consistency (e.g., HBase, MongoDB in some configurations).
- **AP systems** sacrifice consistency for availability (e.g., Cassandra, DynamoDB).
- **CA** systems are typically only achievable in single-node or non-partitioned environments.

The CAP theorem helps guide decisions in distributed system design, particularly around how the system should behave under network partitions.

#### Comparison Table of CAP Theorem Trade-offs

| Type | Guarantees                        | Sacrifices     | Use Cases                                 |
|------|-----------------------------------|----------------|--------------------------------------------|
| CP   | Consistency, Partition Tolerance  | Availability   | Financial systems, master-slave databases  |
| AP   | Availability, Partition Tolerance | Consistency    | DNS, caching layers, shopping carts        |
| CA   | Consistency, Availability         | Partition Tolerance | Single-machine systems, tightly-coupled clusters |

### PACELC Theorem

The PACELC Theorem is an extension of CAP and provides a more nuanced view by introducing latency and consistency trade-offs even when there is no partition.

PACELC stands for:
- **If Partition (P)** occurs: trade off **Availability (A)** or **Consistency (C)**
- **Else (E)**, when the system is running normally: trade off **Latency (L)** or **Consistency (C)**

This model captures the reality that distributed systems often face performance trade-offs even in the absence of network partitions.

#### Comparison Table of PACELC Trade-offs

| System     | P: Partition Handling | E: Latency vs. Consistency | Notes                                  |
|------------|-----------------------|-----------------------------|----------------------------------------|
| DynamoDB   | AP                    | EL                          | Optimised for availability and latency |
| Cassandra  | AP                    | EL                          | Tunable consistency, highly available  |
| Bigtable   | CP                    | EC                          | Prioritises consistency even at cost of latency |
| Spanner    | CP                    | EC                          | Uses TrueTime to provide strong consistency |


### Client Interactions

Client-server interactions are a core part of modern distributed system design. Depending on the use case, you may need one-way, two-way, or real-time communication. Below are the most common approaches, categorised by interaction pattern.

#### 1. Pull-Based Communication (Client Initiates)

- **Polling**: The client periodically requests data from the server, regardless of whether new data is available.
- **Long Polling**: The client sends a request that the server holds open until new data is available, improving latency over regular polling.
- **HTTP/2 Server Push**: Server pushes resources it anticipates the client will need. Technically initiated by the client’s request but can feel server-initiated.

#### 2. Push-Based Communication (Server Initiates)

- **Server-Sent Events (SSE)**: Server pushes updates to the client over a single HTTP connection (one-way, text/event-stream format).
- **Web Push Notifications**: Server sends notifications to client devices via push services, typically when the browser or app is not actively open.
- **WebHooks**: Server sends an HTTP POST to a configured endpoint when an event occurs. Common in third-party integrations.

#### 3. Bidirectional Communication (Real-Time Two-Way)

- **WebSockets**: Full-duplex communication channel over a single, long-lived TCP connection. Suitable for chat, gaming, collaborative editing.
- **gRPC Streaming**: Supports bidirectional streaming over HTTP/2. Useful in low-latency service-to-service or mobile communication.
- **GraphQL Subscriptions**: Typically built on WebSockets; enables real-time data updates in GraphQL APIs.
- **MQTT**: Lightweight, publish-subscribe messaging protocol, often used in IoT and mobile messaging.
- **XMPP**: Extensible Messaging and Presence Protocol. Legacy protocol for chat and presence, supports real-time messaging.

#### 4. Hybrid/Other

- **Comet**: A legacy term referring to techniques like long polling or streaming used before WebSockets became standardized.
- **Fallback Strategies**: Systems often implement fallback mechanisms (e.g., WebSockets falling back to long polling) to maintain functionality across diverse client environments.


#### Comparison Table of Client Interaction Mechanisms

| Mechanism               | Direction         | Protocol         | Real-Time | Complexity | Use Cases                                      |
|------------------------|-------------------|------------------|-----------|------------|------------------------------------------------|
| Polling                | Client → Server   | HTTP             | No        | Low        | Low frequency updates, legacy systems         |
| Long Polling           | Client → Server   | HTTP             | Near-Real | Medium     | Chat apps, presence systems                   |
| HTTP/2 Server Push     | Server → Client   | HTTP/2           | Yes       | Medium     | Optimising page load times                    |
| Server-Sent Events     | Server → Client   | HTTP             | Yes       | Low        | News feeds, stock tickers                     |
| Web Push Notifications | Server → Client   | HTTP             | Yes       | High       | Alerts, background updates                    |
| WebHooks               | Server → Client   | HTTP POST        | Yes       | Medium     | Event-driven integrations                     |
| WebSockets             | Bi-directional    | TCP/WS           | Yes       | High       | Real-time collaboration, games                |
| gRPC Streaming         | Bi-directional    | HTTP/2           | Yes       | High       | Service-to-service communication              |
| GraphQL Subscriptions  | Bi-directional    | WebSocket        | Yes       | High       | Real-time GraphQL data updates                |
| MQTT                   | Bi-directional    | MQTT             | Yes       | Medium     | IoT, lightweight mobile messaging             |
| XMPP                   | Bi-directional    | TCP/XMPP         | Yes       | High       | Messaging, presence, legacy chat systems      |
| Comet                  | Mixed             | HTTP             | Near-Real | Medium     | Legacy browser-based apps before WebSockets   |

This table highlights the trade-offs between various mechanisms, helping architects select the appropriate one based on latency needs, protocol support, and implementation complexity.

### Bloom Filters

### Quorum Algorithms

### Leaders and Followers

### Heartbeat and Alive

### Consistent Hashing

### Checksums and Signatures

### Eventual Consistency vs Strong Consistency

In distributed systems, consistency refers to the degree to which all nodes in a system reflect the same data at any given time. Two common models are eventual consistency and strong consistency, and each has its place depending on system requirements.

**Strong Consistency** ensures that once a write operation is completed, all subsequent reads will return that updated value. This is ideal in systems where correctness and synchronization are critical, such as in banking transactions, inventory systems, or systems with strict business rules. Strong consistency often relies on coordination mechanisms such as distributed consensus algorithms (e.g., Paxos or Raft) and can result in higher latency and reduced availability, especially under network partitions.

**Eventual Consistency**, on the other hand, guarantees that if no new updates are made to a given data item, eventually all accesses to that item will return the last updated value. It is commonly used in systems designed for high availability and partition tolerance (e.g., DynamoDB, Cassandra). Eventual consistency favors availability over immediate consistency, and is often acceptable in scenarios like user profile updates, feeds, or analytics systems, where stale reads for a short time are tolerable.

The choice between these models is guided by the [CAP theorem](https://en.wikipedia.org/wiki/CAP_theorem), which states that a distributed system can only guarantee two out of three properties: Consistency, Availability, and Partition Tolerance. Systems must often trade off consistency for higher availability and resilience in partitioned networks, making eventual consistency a popular choice in internet-scale applications.

### Real-World Example: Payments Systems

Consider the design of a real-time payment processing system, such as one used by a bank or payment gateway. These systems typically require **strong consistency** to ensure that money is debited and credited accurately, and that no funds are lost or duplicated. For example, when a customer transfers money between accounts, it's crucial that the transaction either completes in full or not at all — a classic case for ACID-compliant systems using strong consistency.

However, peripheral components in the same ecosystem, such as notification systems, fraud detection, or analytics platforms, may rely on **eventual consistency**. These services are often updated asynchronously to avoid delaying the critical payment path. For instance, a user might receive a payment confirmation email a few seconds after the transaction has completed — which is acceptable from a user experience standpoint.

This blend of consistency models — strong for the core transaction, eventual for supporting services — is common in distributed financial systems where performance, reliability, and user trust must be carefully balanced.


### ACID and BASE

When designing storage systems, particularly databases and data services, two contrasting models often come up: **ACID** and **BASE**. These models represent different approaches to data integrity, availability, and consistency in distributed environments.

**ACID** stands for Atomicity, Consistency, Isolation, and Durability. It is the traditional model used in relational databases:
- **Atomicity** ensures that a transaction is all-or-nothing.
- **Consistency** guarantees that a transaction brings the database from one valid state to another.
- **Isolation** ensures that concurrent transactions do not interfere with each other.
- **Durability** guarantees that once a transaction is committed, it will persist even in the face of system failures.

ACID transactions are critical in domains where data integrity and correctness are paramount, such as banking, inventory, and order management systems.

**BASE**, on the other hand, is often associated with NoSQL and distributed systems designed for scale:
- **Basically Available** means the system guarantees availability, even under failure.
- **Soft state** implies that the state of the system may change over time, even without input (due to eventual consistency).
- **Eventual consistency** means that while the system may not be consistent at a given point, it will become consistent over time.

BASE systems are better suited for applications that require high availability and can tolerate some temporary inconsistency — such as content delivery, social feeds, or recommendation engines.

Understanding the ACID vs BASE trade-off helps architects make informed decisions about which data model best aligns with the system’s requirements for reliability, performance, and scale.

### Latency vs Throughput

### Caching - Read vs Write

### Batch vs Real-time Streaming

### Load Balancing and API Gateways

### Proxy and Reverse Proxy

### CDN

### API Gateway vs Reverse Proxy

### SQL vs NoSQL vs Other

### Serverless vs Traditional

### Primary - Replica vs Peer-to-Peer

### Stateful vs Stateless

###

## Trade-offs

Presenting trade-offs in a system design interview is highly significant for several reasons as it demonstrates a depth of understanding and maturity in design. Here’s why discussing trade-offs is important:

1. Shows Comprehensive Understanding

Balanced Perspective: Discussing trade-offs indicates that you understand there are multiple ways to approach a problem, each with its advantages and disadvantages.
Depth of Knowledge: It shows that you're aware of different technologies, architectures, and methodologies, and understand how choices impact a system's behavior and performance.
2. Highlights Critical Thinking and Decision-Making Skills

Analytical Approach: By evaluating trade-offs, you demonstrate an ability to analyze various aspects of a system, considering factors like scalability, performance, maintainability, and cost.
Informed Decision-Making: It shows that your design decisions are thoughtful and informed, rather than arbitrary.
3. Demonstrates Real-World Problem-Solving Skills

Practical Solutions: In the real world, every system design decision comes with trade-offs. Demonstrating this understanding aligns with practical, real-world scenarios where perfect solutions rarely exist.
Prioritization: Discussing trade-offs shows that you can prioritize certain aspects over others based on the requirements and constraints, which is a critical skill in system design.
4. Reveals Awareness of Business and Technical Constraints

Business Acumen: Understanding trade-offs indicates that you're considering not just the technical but also the business implications of your design choices (like cost implications, time to market).
Adaptability: It shows you can adapt your design to meet different priorities and constraints, which is key in a dynamic business environment.
5. Facilitates Better Team Collaboration and Communication

Communication Skills: Clearly articulating trade-offs is a vital part of effective technical communication, crucial for collaborating with team members and stakeholders.
Expectation Management: It helps in setting realistic expectations and preparing for potential challenges in implementation.
6. Prepares for Scalability and Future Growth

Long-term Vision: Discussing trade-offs shows that you’re thinking about how the system will evolve over time and how early decisions might impact future changes or scalability.
7. Shows Maturity and Experience

Professional Maturity: Recognizing that every decision has pros and cons reflects professional maturity and experience in handling complex projects.
Learning from Experience: It can also indicate that you’ve learned from past experiences, applying these lessons to make better design choices.
Conclusion

## Conclusion

System design is about managing complexity through deliberate choices. Each decision — from consistency models to caching strategies — involves trade-offs that influence the system’s behaviour under load, failure, and change. Understanding these patterns empowers architects and engineers to build resilient, scalable, and maintainable systems in an ever-evolving technological landscape.