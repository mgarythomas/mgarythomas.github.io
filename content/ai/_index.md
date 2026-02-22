---
title: "AI"
summary: "AI related posts"
draft: true
tags: ["ai"]
categories: ["ai"]
author: "Gary Thomas"
date: 2025-04-26
---

# What are agents?

Agents are AI systems powered by Large Language Models (LLMs) that use tools to perform complex tasks. Beyond simple question-answering, intelligent agents can perceive their environment, reason about how to solve problems, and take autonomous actions to achieve goals—ranging from deep research to precise data extraction.

# What are workflows?

Workflows are structured, multi-step processes that orchestrate agents, data connectors, and tools to accomplish complex objectives. By combining Retrieval-Augmented Generation (RAG) with agentic capabilities, workflows enable advanced behaviors like self-reflection and error-correction. These event-driven applications can be deployed as production-ready microservices to handle sophisticated tasks with reliability.

# What is context augmentation?

LLMs offer a natural language interface between humans and data. While they come pre-trained on vast amounts of public knowledge, they lack access to your specific data—whether it's private, domain-specific, or locked away in APIs, SQL databases, and PDF documents.

Context augmentation bridges this gap by making your proprietary data available to the LLM. Frameworks like LlamaIndex provide the toolkit to build context-aware use cases, from prototype to production. These tools allow you to ingest, parse, index, and process data to implement complex query workflows that combine data access with LLM reasoning.

The most prominent example of context augmentation is Retrieval-Augmented Generation (RAG), which dynamically retrieves relevant context for the LLM at inference time.

# What is Backpropagation?

Backpropagation is the fundamental algorithm that allows neural networks to learn from their mistakes.
Here's how it works: When a neural network makes a prediction, we compare it to the correct answer and calculate an error (or "loss"). Backpropagation is the process of sending that error backward through the network to figure out how much each connection (weight) contributed to the mistake.
Think of it like tracing responsibility through a chain of decisions. Imagine a company fails to meet a deadline. To improve, you'd trace back through the process: Was it the final assembly team? The parts supplier? The initial planning? Each step gets assigned some portion of the blame based on how much it contributed. Backpropagation does exactly this mathematically for neural networks.

## The process:

- Forward pass: Input data flows through the network, layer by layer, producing a prediction
- Calculate error: Compare the prediction to the actual answer
- Backward pass: Starting from the output, calculate how much each weight contributed to the error using the chain rule from calculus
- Update weights: Adjust each weight slightly to reduce the error (this is where gradient descent comes in)

