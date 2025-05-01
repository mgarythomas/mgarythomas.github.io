---
title: "Building Blocks"
description: "TOGAF Building Blocks (BB) of the Architecture"
draft: false
ShowToc: false
TocOpen: false
tags: ["Building Blocks","ABB","SBB", "togaf"]
categories: ["architecture"]
author: "Gary Thomas"
date: 2025-03-10
---

# Building Blocks

## Overview

These are potentially re-usable components that can be used to deliver an Architecture.
TOGAF will group these into the abstract Logical - Application Building Blocks and the Physical Building Blocks - Solution Building Blocks (SBB).
Without being too prescriptive, a building block should meet the following criteria:
- Is a package of functionality defined to meet a business need or capability. It should be recognisable as a discrete thing.
- Should normally correspond to one of the types defined in the Enterprise Metamodel - Actor, Business Service, Application or Data Entity.
- Can be defined at various levels of detail depending on the objective of the Architecture and also the Phase.
- There is a general benefit of composing functionality through building blocks in that it should improve integration and interoperability through defined interfaces and contracts. It may also improve reusability and flexibility through the creation of new re-usable applictions or components.

![TOGAF Building Blocks](/images/architecture/togaf/buildingBlocks.gif)

## Criteria

The following list is not exhaustive but serves as a basis for determing the correct building blocks:
- Is re-usable and replaceable with clear specification of interfaces and contracts
- May be assembled from other Building Blocks or form a sub-component of another Building Block. i.e. Building Blocks are composable.
- Considers the implementation and usage of the component within the Architecture so that it independently satisfies the needs of the business. It should evolve over time and exploit technology changes.
- Interoperates with other independent Building Blocks through a published and stable interface.
- Should have defined boundaries and specification
- Loosely coupled to the implementation i.e. It is possible to realize a building block in different ways.

![TOGAF Building Blocks Phases](/images/architecture/togaf/buildingBlocksPhases.gif)

## Architecture Building Blocks (ABB)

These are special types of Building Blocks that are used to describe the required capability in a Logical or Vendor agnostic way.

## Solution Building Blocks (SBB)

Solution Components that realise the required capability (as defined in an ABB) but now with a physical implementation.

As shown below:

![TOGAF ABB to SBB Building Blocks](/images/architecture/togaf/abbSbbRelationship.svg)

