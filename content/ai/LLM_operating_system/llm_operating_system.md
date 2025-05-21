---
title: "LLM Operating System"
description: "An overview of the LLM Operating Syste (OS) and why it is important. An agent architecture that supports a memory hierarchy."
draft: true
ShowToc: false
TocOpen: false
author: "Gary Thomas"
date: 2025-05-19
---

## Introduction

The LLM Operating System (LLM OS) is an agent architecture that supports a memory hierarchy.

It is based on a research paper [MemGPT](https://arxiv.org/abs/2310.08560) which attempts to address the challenges of the interactions with an LLM being constrained by the size of the context window.

The LLM OS is a collection of agents that work together to perform a task. Each agent has a specific role and is responsible for a specific aspect of the task.

### Memory Management

The LLM OS moves data in and out of the context window in order to manage memory (according to constraints of the LLM and processing).

### Memory Hierarchy

The Hierarchy is a means for the LLM OS to divide the LLM's memory into two parts:

1. In-Context Memory (Working Memory)
2. Out-of-Context Memory

### Self-Editing Memory

In MemGPT the Operating System that manages memory, what is in and out of context, is itself an LLM. The LLM moves data in and out of the context window using designated memory-editing tools (Where tools follow the standard LLM tool designation).

### Multi-Step Reasoning

The MemGPT model describes a mechanism for an Agent to support multi-step reasoning (Allowing the agent to take multiple steps in sequence. adding responses to the context to allow the LLM to think again in a loop). Whenever the LLM outputs a tool call it can choose to execute another step in the loop - MemGPT and [letta](https://docs.letta.com/) refer to this as *request_heartbeat* which is set to true.
