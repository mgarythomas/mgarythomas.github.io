---
title: "Architecture"
summary: "A summary of various thoughts and posts on architecture."
draft: false
tags: ["definition", "togaf"]
categories: ["architecture"]
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

# Standing on the shoulders of giants
I wasn't sure where to start with the description of architecture, but I have read so much different content over time that it is worth calling out so many people who have helped shape my thinking. In no particular order:

| Name | Description |
| --- | --- |
| [Gregor Hohpe](https://architectelevator.com/)| Probably needs no introduction from me, but the man who started with the EAI book and has since become a leading authority on architecture and always an interesting read, has worked for some influential companies but retains an independent voice. |
| [Martin Fowler](https://martinfowler.com/) | Martin Fowler is an author and expert on the development of software and has produced a number of influential publications on the subject. |
| [Eric Evans](https://www.domainlanguage.com/ddd/) | Eric Evans is a software engineer and author who is known for his work on Domain Driven Design (DDD) as a means to address the complexity of large software systems. When I first read this, a light went one but it took me a while to understand how to make it work in practice |
| [Adrian Cockcroft](https://www.linkedin.com/in/adriancockcroft/)| The man behind Netflix's move to cloud and a leader in Cloud Architecture|
| [Robert C. Martin](http://blog.cleancoder.com/) | Also known as "Uncle Bob", Martin is a software engineer and author who has written extensively on software architecture and design. He is the founder of the Agile Software Development movement and is known for his work on the principles of software architecture. |
| [Donella Meadows](https://en.wikipedia.org/wiki/Dana_Meadows) | Dana Meadows was a systems theorist and author who was a pioneer of systems thinking. She is best known for her work on the World3 computer model, which was a simulation of global population, industrial growth, and resource depletion. |
| [Kaine Ugwu](https://www.kaine.pro/my-story) | Kaine Ugwu thinks about architecture and provides a lot of insight into strategy and how this works in practice. |
| [David Farley](https://www.davefarley.net/) | A software engineer and architect with lits of real-world experience that comes through in his practical thoughts on how to deliver software and design systems |
| [Grady Booch](https://en.wikipedia.org/wiki/Grady_Booch) | Grady Booch is a software engineer and author who is known for his work on the principles of software architecture. He is the founder of the Object Management Group (OMG) and is the inventor of the Unified Modeling Language (UML). I still love the use of clouds instead of boxes as these were an over-used metaphor, but it introduced me to the idea of how to visualise the architecture of a software system. |
| [Jeff Langr](https://www.langrsoft.com/about/) | Jeff Langr is a software engineering veteran and author who is known for his work on the principles of software architecture and contributor to the books Clean Code and Clean Agile. A member of the Pragmattic Programmers technical advisory board. |

The list goes on...
---

# Why do we have architecture?
The purpose of architecture is to communicate to all stakeholders what the system is, how it functions, and how it is expected to perform. It serves as an alignment between the business strategy and requirements and the technology architecture designed to fulfil those needs.

Through various assignments in architecture, I’ve observed that architects often define their architectural views primarily for the benefit of other architects. This focus is especially evident in approaches like ArchiMate. However, if our aim is to harmonise business strategy with technology architecture, our stakeholders are both business and technology. Therefore, it is essential to present views that are understandable to both groups — though not necessarily within a single unified view.

This is not an argument against the use of different architectural views. On the contrary, multiple views are necessary to convey the different levels of detail required by various stakeholders. What I often observe, however, is an emphasis either on the business concerns or the technology concerns, without sufficient effort to harmonise both.

For a deeper understanding of the [purpose](/architecture/togaf/purpose) of enterprise architecture, as defined in the TOGAF Standard, I have provided a summary.

This section will also explore various architecture frameworks and approaches.