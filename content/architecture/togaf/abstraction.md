---
title: "Architecture Abstraction"
description: "Architecture Abstration Levels"
draft: true
weight: 40
ShowToc: false
TocOpen: false
tags: ["abstraction"]
categories: ["architecture", "togaf"]
author: "Gary Thomas"
---

# Architecture Abstraction

The concept of abstraction is a means to enable reasoning about an Architecture. Dividing a problem into smaller problems is a common approach to making an Architecture easier to model and create solutions for.

We can have one or more of the abstraction levels at each of the Strategic, Segment or Capability Architecture.

## Introduction

We can consider multiple simple questions in order to structure the approach to abstraction:

1. *Why* - Contextual, why do we need the Architecture?
2. *What* - What are the Strategy and requirements that need to be met by the Architecture?
3. *How* - (Logical) How do we structure the required capabilities/functionality?
4. *With* - What are the Physical Assets we can use to implement the Architecture?

## Definitions

|Level|Description|
|---|---|
|Contextual Abstraction|- Understand the Environment of an Enterprise and the contect of the Architecture|
| |- Scope, Motivation, Drivers, Objectives, Constraints, and Goals|
|Conceptual Abstraction|- Understand the problem and the requirements of the Architecture|
| |- Business Services, Application Services, Technology Services|
|Logical Abstraction|- Identify *Implementation Independent Components* to achieve the required services of the Conceptual Abstraction|
|Physical Abstraction|- Find alternatives for the implementation of the Physical Components to meet the Logical Abstraction|