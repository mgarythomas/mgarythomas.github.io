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

### Proxies

### Redundancy

### Replication

### Data - NoSql and Sql

### CAP Theorem

### PACELC Theorem

### Client Interactions - Long Polling, Web Sockets, Server Sent Events, Push Notifications, WebHooks

### Bloom Filters

### Quorum Algorithms

### Leaders and Followers

### Heartbeat and Alive

### Consistent Hashing

### Checksums and Signatures


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

In system design interviews, discussing trade-offs is not just about acknowledging that they exist, but about demonstrating a well-rounded and mature approach to system design. It reflects a candidate’s ability to make informed decisions, a deep understanding of technical principles, and an appreciation of the broader business context.



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

## Conclusion

System design is about managing complexity through deliberate choices. Each decision — from consistency models to caching strategies — involves trade-offs that influence the system’s behaviour under load, failure, and change. Understanding these patterns empowers architects and engineers to build resilient, scalable, and maintainable systems in an ever-evolving technological landscape.