---
title: "Methodology"
summary: "An approach to Strategy and Architecture"
draft: true
weight: 20
ShowToc: false
TocOpen: false
url: "/architecture/methodology"
tags: ["methodology", "strategy"]
categories: ["architecture"]
author: "Gary Thomas"
---

# Overview

TOGAF defines levels of architecture within an Architecture Landscape:
- Strategic
- Segment
- Capability

For simplicitly, Business capabilities can exist at different levels as well. Even when we are dealing with architecture at a Strategic level we would expect that to encompass business capabilities at a broader level.

If we look at the example of BIAN it groups capabilities at a high-level (note this is only a partial view):

*Whole of Enterprise*
- Enterprise Management and Controlling
    - Businesss Direction Management
    - Policy Management
    - Business Entity Management
    - Risk Management
    - Fraud Incident Management
    - Finance Management
        - Financial Account Management
        - Tax Management
        - Financial Position Management
- Product and Service Enabling
- Enterprise Enabling
- Marketing and Sales
- Customer and Distribution

# Methodology

While TOGAF has a phased view and iterations, for simplicity I have broken down the steps of the approach to align to simpler terms.

*Note that key TOGAF terms are shown in red, these are a mix of phases and artifacts.

![Methodology](/images/architecture/methodology.png)

## Strategy
Capture the Business Strategy, this usually exists in some format, from an architecture approach it can be helpful to standardise how this is presented.
Provide metrics that can be used to measure the succss of the strategic goals.
Gather the architecturally significant business requirements, at a sufficient level of detail to be able to inform the subsequent steps in the process
Develop a set of Principles that are used to inform the architectural decisions. Validate that these hold true to the Business Strategy
Define the scope and develop a Business Capability model for the level of architecture


## Current State
This is what TOGAF refers to as the Baseline.

Capture the different components for current Business, Data, Application and Technology states. These can happen in parallel.
Provide a consistent mapping to Business Capability so that this can be used to identify the gaps between current state and target state.
Additionally consider changes to the Operating Model that will occur with the realisation of Business Strategy.
Ensure that the architecture considers all required Cyber Security requirements and these are baked into the Architecture.

## Target State
The same components as Current State but now defining those elements required to realise the Strategic goals.

TOGAF has a view of Application Building Blocks (ABB) and Solution Building Blocks (SBB) which are useful in defining reusable components.

## Roadmap
Provide prioritised transition steps for all of the components to reach the Target State.

## Enablement
Provide the artifacts that will enable the delivery of the approved architecture

## Execution
Deliver the architecture and realise Business Strategy
This requires a lot of different elements including all of the Delivery Management, Product and Experience Design, Data and Process modelling, Solution Architectures, Designs, Engineering, Build Processes, Infrastructure, Security and Operationalisation. (This list is not meant to be exhaustive but indicative)
It is not intended to explain the details of all of these different parts of delivery as they deserve a complete definition of their own!