---
title: "Architecture"
summary: Architecture Overview
draft: true
weight: 20
tags: ["definition"]
categories: ["architecture", "togaf"]
author: "Gary Thomas"
---

# What is architecture?

It is quite difficult to provide a definition for a fundamental concept like architecture. As it will form the basis for everything that follows it needs to be clear and hopefully unambiguous. As a previous colleague not unreasonably said "Is architecture even a thing?".
We seems to jumpt co classify different types of architecture - enterprise, application, cloud, system, etc, while  fundamentally missing the definition of what it is and how it distinguishes itself from its near neighbour **design**. I like that Robert C. Martin ("Uncle Bob") argues that there is no distinction between architecture and design. That an architect for a building will go from not just the outline of the building to some of the very low-level details, which is something that an architect of technology and software will also do.

The low-level details and the high-level details are the same, the only difference is the scale at which we are looking at the system. What becomes very apparent in practice is that some developers can look at the micro-level and focus on the design of specifics without being able to envisage the macro-level of the whole system.

The most consistent elements of these definition relate to it being a shared understanding of a system or systems and their components. This means that features of an architecture would also include:
- The structure of the various components including the infrastructure they require
- The relationships between the components how they integrate and the means of interaction and communication
- The standards, principles and guidelines governing the design and evolution of the system
- How it meets the requirements of resilience, scalability, performance, security, etc. I don't like referring to these as non-functional requirements as they are very much a requirement of the architecture and a desired outcome of the architecture.

> The fundamental concepts or properties of a
> system in its environment embodied in its elements,
> relationships and in the principles of its design &
> evolution.
> 
> (Source: ISO/IEC/IEEE 42010: 2011)

# Why do we have architecture?
It is to communicate to all the stakeholders what the system is, how it works, and how it is expected to perform. It is also an alignment between the Business Strategy and Requirements and the Technology Architecture that is to realise that strategy and requirement.

What I have found through many different architecture assignments is that architects seem to define the views of their architecture for the benefit of other architects - I am looking at you Archimate!
Yet, if we are harmonising the business strategy with the technology strategy and architecture *our Stakeholders are both business and technology*. We must present views that are understandable by both, though not necessarily in a single view.

I am not arguing against the use of views, this is a necessity to provide the levels of detail required by the different stakeholders, but repeatedly I see architects focus on the concerns of the business **OR**  the concerns of the technology and are not good at harmonising both.

I have provided a summary of the [purpose](/architecture/togaf/purpose) of an enterprise architecure as defined in the TOGAF Standard.

This section contains information about various architecture frameworks and approaches: