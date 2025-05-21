---
title: "Event-Driven Architecture"
description: "An introduction to Event-Driven Architecture and best practices."
draft: true
ShowToc: false
TocOpen: false
tags: ["event-driven", "architecture"]
categories: ["engineering"]
author: "Gary Thomas"
date: 2025-05-18
---

# Event-Driven Architecture

Event-Driven Architecture (EDA) is a design approach that uses events to drive the flow of data and actions within a system. Events are used to represent changes in the system, and these events are used to trigger actions in other parts of the system.

## Commands and Events

In systems designed with Domain-Driven Design, commands and events typically correspond to actions and outcomes within specific bounded contexts.

Event driven architectures often use a combination of both commands and events, the decision of whent to use each is based on the use case and the requirements of the system.

### Commands

Commands are used to represent requests for actions that are taken by the system, these are often used to represent user actions or system actions that are taken to change the state of the system.
A command is an instruction and is normally directed to an intended recipient.
The command will normally generate a notification that represents an event that has occurred (state change).

### Events

Events are used to represent changes in the system, these are often used to represent changes in the state of the system or changes in the data within the system.
They are immutable and are raised *after* the action has occurred. 
The use of events encourages loose-coupling between the system and the components that consume the events as the consumers are not aware of the producer of the events.

### Event Sourcing

Event sourcing is a pattern where the state of the system is stored as a sequence of events. This is often used to represent the history of the system and is used to rebuild the state of the system.
A state model is used to represent the current state of the system by replaying the sequence of events.

### Command Query Responsibility Segregation (CQRS)

CQRS is a pattern where the read and write models of the system are separated. This is often used to represent the different concerns of the system and is used to improve the performance of the system. 
The write operations are represented by Commands. The control flow of the system is easier to reason about as the write model is separated from the read model.
This pattern is often used in conjunction with event sourcing and Domain-Driven Design to better capture intent and optimise performance.

### Event Versioning

Event-driven architectures, on the other hand, are still bound by lesser forms of coupling such as schema coupling. As a system changes over time the number of events and the content of the events can (or more likely will) change.

#### Version Number in the event name

One way to handle this is to include a version number in the event name. This allows the consumer to determine which version of the event to process.

#### Version Name in the event schema (payload)

Another way to handle this is to include a ver  sion name in the event schema. This allows the consumer to determine which version of the event to process.

[CloudEvents](https://cloudevents.io/) is a specification for event data exchange. It defines a set of standard attributes that can be used to describe an event, including the event type, source, and time. It also defines a set of standard extensions that can be used to describe additional attributes of an event.

#### Different topics or streams

Another way to handle this is to use different topics or streams for different versions of the event. This allows the consumer to determine which version of the event to process.

#### Schema Registry

Another way to handle this is to use a schema registry to manage the different versions of the event schema. This allows the consumer to determine which version of the event to process with the schema id included in the event metadata.

#### No Breaking Changes of additions only

Another way to handle this is to only add new fields to the event schema and never remove or change existing fields. This allows the consumer to determine which version of the event to process with the schema id included in the event metadata.

#### Out of Band Schema Translation

This requires additional complexity with an intermediary consumer responsible for translation of the event schema to the consumer's expected schema. This is often used in event-driven architectures where the consumer is not aware of the producer of the event.

---

## When to Push or Poll

### Push based Events

Push based events are where the event is sent to the consumer as soon as it is available. This is commonly used for pub/sub architectures.

#### Benefits

* Low end-to-end latency
* Simple to implement
* No polling overhead, no wasted compute cycles
* Notifications, fan-out and triggering workflows

#### Drawbacks

* Harder to control throughput
* More complex to manage back-pressure 
* Required additional logic to handle consumer failures and retries, dead-letter-queues (DLQ)

### Poll based Events

Poll based events are where the consumer polls the event store for new events. This is less common and is used in some event-driven architectures where the consumer needs to be able to process events in a specific order.

#### Benefits

* Easier to control throughput and concurrency
* Consumers can make decisions about checkpoints and also re-try logic.
* Fault tolerance in processing easier to achieve

#### Drawbacks

* Higher end-to-end latency, dependent on polling interval
* More infrastructure required to manage the event store (sharding, offsets groups, etc.)

### Bounded Context Scenario

To further illustrate the concepts of commands, events, and bounded contexts in a Domain-Driven Design (DDD) environment, consider the example of an online retail platform. The system is composed of several bounded contexts, each owning its domain logic and data.

#### Bounded Contexts

- **Order Management**
- **Inventory Management**
- **Payment**
- **Shipping**

Each context communicates asynchronously using domain events, ensuring loose coupling and autonomy.

#### Example Flow: Customer Places an Order

**1. Order Management**
- Command: `PlaceOrder` — triggered by a customer via the web interface.
- The context persists the order with a “Pending” status.
- Event Emitted: `OrderPlaced`.

**2. Inventory Management**
- Listens for the `OrderPlaced` event.
- Checks inventory and issues the `ReserveStock` command.
- Emits: `StockReserved` or `StockNotAvailable`.

**3. Payment**
- Listens for `StockReserved`.
- Processes payment via the `ProcessPayment` command.
- Emits: `PaymentConfirmed` or `PaymentFailed`.

**4. Shipping**
- Listens for `PaymentConfirmed`.
- Initiates shipment via the `CreateShipment` command.
- Emits: `ShipmentCreated`.

#### Summary of Concepts

| Concept               | Role in Scenario                                         |
|----------------------|----------------------------------------------------------|
| **Command**           | Represents intent (e.g., `PlaceOrder`, `ProcessPayment`) |
| **Event**             | Represents outcome (e.g., `OrderPlaced`, `StockReserved`) |
| **Bounded Context**   | Encapsulates domain-specific logic and data              |
| **Loose Coupling**    | Communication via asynchronous events                    |
| **Scalability & Fault Tolerance** | Contexts operate and scale independently              |

