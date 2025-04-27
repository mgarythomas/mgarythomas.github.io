---
title: "Agentic AI Frameworks"
summary: "Agentic AI Frameworks a brief comparison"
draft: true
tags: ["ai", "agentic", "frameworks"]
categories: ["ai"]
author: "Gary Thomas"
date: 2025-04-26
---

Frameworks for generating Agentic applications (Building AI Agents) have been around for a while now.

I wanted to start curating a list as some of these are very new - and I imagine that the list will keep on growing

| Name | Version | Description |
|------|---------|-------------|
|[Autogen](https://microsoft.github.io/autogen/)|0.5|A framework that enables the development of AI agents and applications.|
|[CrewAI](https://www.crewai.com/)|0.114|CrewAI is a python framework built entirely from scratch—completely independent of LangChain or other agent frameworks.|
|[LangGraph](https://www.langchain.com/langgraph)|0.1.0|LangGraph is an orchestration framework for building complex agentic systems.|
|[ChatDev](https://chatdev.ai/)|0.1.0|The primary objective of ChatDev is to offer an easy-to-use, highly customizable and extendable framework, which is based on large language models (LLMs) and serves as an ideal scenario for studying collective intelligence|
|[Agno](https://www.agno.com/)|0.1.0|Agno is a framework for building, shipping and monitoring AI agents and applications.|
|[Gryffin](https://www.gryffin.ai/)|0.1.0|Gryffin is a framework for building, shipping and monitoring AI agents and applications.|
|[SmolAgents](https://huggingface.co/docs/smolagents/index)|0.1| A simple framework from [Hugging Face](https://huggingface.co/) to build powerful agents|
|[Mastra](https://mastra.ai/)|0.1.0| Mastra is a typescript AI framework.|
|[LlamaIndex](https://docs.llamaindex.ai/en/stable/)|0.1.0| LlamaIndex is a framework for building LLM-powered agents over your data with LLMs and workflows.|
|[Pydantic AI](https://ai.pydantic.dev/)|0.1.0| Pydantic AI is a Python agent framework designed to make it less painful to build production grade applications with Generative AI|
|[Atomic Agents](https://brainblend-ai.github.io/atomic-agents)|1.0.19| A lightweight and Modular Framework for Building AI Agents|
|[AgentOS](https://ag2.ai/)|0.1.0| An end-to-end platform for multi-agent automation.|


## AutoGen

Microsoft released it on Oct. 2023 in collaboration with teams from Penn State University, and the University of Washington. Version 0.2 was probably the defacto version but there is a new and updated version available which changed from version 0.4 forward. This also supports MCP (Model-Context Protocol).

The name was taken from the Aristotle quote:
> "The whole is greater than the sum of its parts"
> - Aristotle

Here's how they describe it:
AutoGen is a framework for building AI agents and applications. At its core it is an event-driven python framework for building scaleable multi-agent AI systems.

## CrewAI

CrewAI empowers developers with both high-level simplicity and precise low-level control, ideal for creating autonomous AI agents tailored to any scenario:

* *CrewAI Crews*: Optimize for autonomy and collaborative intelligence, enabling you to create AI teams where each agent has specific roles, tools, and goals.
* *CrewAI Flows*: Enable granular, event-driven control, single LLM calls for precise task orchestration and supports Crews natively.