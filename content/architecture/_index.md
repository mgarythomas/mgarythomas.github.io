---
title: "Architecture"
summary: "A summary of various thoughts and posts on architecture."
draft: true
weight: 20
tags: ["definition"]
categories: ["architecture", "togaf"]
author: "Gary Thomas"
---

# What is architecture?

Defining architecture can be a challenging task, especially given its fundamental role across various domains. To set a clear foundation for everything that follows, we must establish a definition that is both precise and unambiguous. A former colleague once posed the question, “Is architecture even a thing?” — a question that, while simple, underscores the difficulty in distinguishing architecture from its neighbouring concepts.

Architecture is often categorised into various types — such as enterprise, application, cloud, and system architecture — yet there remains a gap in understanding what architecture fundamentally is and how it differentiates itself from design. Robert C. Martin, also known as “Uncle Bob,” makes an interesting point that in his opinion there is no true distinction between architecture and design. Just as an architect of a building moves from high-level conceptual drawings to detailed specifications, so too does a technology or software architect.

The key difference lies not in the nature of the work but in the scale at which we are working. The high-level and low-level details are interconnected, and in practice, it becomes clear that some developers focus solely on micro-level specifics without being able to visualise the entire system at the macro level.

The most consistent feature of architecture, across domains, is its role as a shared understanding of the system or systems and their components. Therefore, architectural features encompass:
	•	The structure of the components and the infrastructure they require
	•	The relationships between components, their integration, and their communication methods
	•	The principles, standards, and guidelines that govern the design and evolution of the system
	•	How the system meets critical non-functional requirements such as resilience, scalability, performance, and security. These should not be dismissed as “non-functional requirements,” as they are integral to the architecture and represent desired outcomes.

> The fundamental concepts or properties of a system in its environment embodied in its elements, relationships and in the principles of its design and evolution.
> 
> (Source: ISO/IEC/IEEE 42010: 2011)

---

# Why do we have architecture?
The purpose of architecture is to communicate to all stakeholders what the system is, how it functions, and how it is expected to perform. It serves as an alignment between the business strategy and requirements and the technology architecture designed to fulfil those needs.

Through various assignments in architecture, I’ve observed that architects often define their architectural views primarily for the benefit of other architects. This focus is especially evident in approaches like ArchiMate. However, if our aim is to harmonise business strategy with technology architecture, our stakeholders are both business and technology. Therefore, it is essential to present views that are understandable to both groups — though not necessarily within a single unified view.

This is not an argument against the use of different architectural views. On the contrary, multiple views are necessary to convey the different levels of detail required by various stakeholders. What I often observe, however, is an emphasis either on the business concerns or the technology concerns, without sufficient effort to harmonise both.

For a deeper understanding of the [purpose](/architecture/togaf/purpose) of enterprise architecture, as defined in the TOGAF Standard, I have provided a summary.

This section will also explore various architecture frameworks and approaches.