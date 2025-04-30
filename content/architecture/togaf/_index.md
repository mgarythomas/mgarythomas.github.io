---
title: "TOGAF"
summary: TOGAF Architecture Framework
draft: false
weight: 10
ShowToc: true
TocOpen: true
tags: ["domain","state", "togaf"]
categories: ["architecture"]
author: "Gary Thomas"
---

# Overview
This content relates to the TOGAF Standard. The following represent a set of notes I created while originally studying the TOGAF Standard. They are not intended to be an exhaustive summary, but an overview of some of the main points.

The Open Group Architecture Framework (TOGAF) is a framework for the development and management of enterprise architectures. (See [Purpose](/architecture/togaf/purpose) for some rationale as to why this is important)

It is a best practice framework that provides a structured approach for Enterprise Architecture:
- It provides an Enterprise Architecture Framework to develop any kind of architecture in **any context**
- The framework has been developed a collaborative effort through a community.
- It describes a standard cycle of change used to plan, develop, implement, govern and change an architecture. This is described further in [adm](/architecture/togaf/adm).
- Describes the building blocks within an enterprise that can be used to fulfil business capabilities and deliver services.

Consider the definition of Enterprise Architecture, It is made up of 2 separate words to distinguish the different roles of the architect.


# Definition of Enterprise

An Enterprise is any collection of organisations that have a common goal.
- This could be a whole Enterprise or one or more specific areas or business units.
- The Architecture could span multiple Enterprises
- It is considered to be a System
- The Enterprise scope may include suppliers, partners and customers
- An Enterprise may develop and maintain serveral different and *independent* Enterprise Architectures (see also Partitioning)

# Definition of Architecture
 The TOGAF Standard enhances the ISO/IEC/IEEE 42010:2011 terminology
1. The fundamental concepts or properties of a
system in its environment embodied in its elements,
relationships and in the principles of its design &
evolution.
(Source: ISO/IEC/IEEE 42010: 2011)
2. The structure of components, their
interrelationships & the principles and guidelines
governing their design & evolution over time.
(Source: The Open Group TOGAF® Standard —
Introduction and Core Concepts)

# Architecture Domains

The TOGAF standard divides an Enterprise Architecture into 4 Different domains:
- *Business Architecture* - Defines the key business strategy, governance, organisation and key business processes
- *Data Architecture* - Describes the structure of an organisation's conceptual, logical & physical data assets, data management resources
- *Application Architecture* - Provides a blueprint for the individual applications to be deployed, their interactions and their relationships to the core business processes of the organisation.
- *Technology Architecture* - Describes the digital architecture and logical software and hardware components and capabilities and standards that are required to support the deployment of business, data and application services.

# Tailoring

The generic TOGAF framework can be tailored and integrated with other frameworks. 

I find the documentation and approach to this to be not well defined and the approach to tailoring is left to the practitioner. This leads to different view and can be seen as a way of covering up the prescriptive nature of TOGAF and trying to avoid the fact that it can be onerous to adopt.