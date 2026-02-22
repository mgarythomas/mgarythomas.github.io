---
title: "Leverage Points"
description: "Applying Donella Meadows' Framework to Transform Your Architecture Practice"
draft: false
url: "/architecture/system-thinking/leverage_points"
ShowToc: false
TocOpen: false
tags: ["systems-thinking", "banking", "patterns", "complex"]
categories: ["architecture"]
author: "Gary Thomas"
date: 2025-09-01
cover:
  image: "leverage_points_cover.svg"
---

# Leverage Points for System Architects: A Systems Thinking Approach

*Applying Donella Meadows' Framework to Transform Your Architecture Practice*

---

## Introduction

As system architects, we're constantly making decisions about where to focus our efforts. Should we optimise those API timeout values? Redesign the entire microservices topology? Or perhaps advocate for a fundamental shift in how the organisation thinks about system resilience?

The answer lies in understanding **leverage points** - a concept from systems thinking that reveals where small changes can produce big results. Based on Donella Meadows' seminal work on systems intervention, this framework helps architects identify the most effective places to intervene in complex systems.

## What Are Leverage Points?

Leverage points are places within a complex system where a small shift in one thing can produce big changes in everything. Meadows identified twelve leverage points in increasing order of effectiveness - from tweaking parameters (low leverage) to changing paradigms (highest leverage).

**The key insight:** Higher leverage points require less effort to create more significant, lasting change. Changing paradigms transforms everything below, whilst changing parameters has limited systemic impact.

---

## The Hierarchy: From Least to Most Effective

### 12. Paradigm Shifts in Architectural Thinking *(Highest Leverage)*

**The fundamental mindset changes that reshape how we approach architecture**

- Monolithic thinking → event-driven architectures
- Centralised → decentralised systems  
- Efficiency-first → resilience-first design
- Perfect uptime → graceful degradation

*Why this matters: When you change how people think about architecture fundamentally, every decision downstream changes automatically.*

### 11. Organisational Culture and Mindset

**The shared values and approaches that guide architectural decisions**

- Enterprise culture of resilience and experimentation
- Design-for-failure mindset across teams
- "Move fast and break things" vs "Move fast with stable infrastructure"
- Blame-free post-incident culture

### 10. Goals and Purpose of the System

**What the system is actually trying to achieve**

- Business-aligned architectural principles
- Resilience vs efficiency trade-offs
- Customer value focus over technical perfection
- Time-to-market vs system stability priorities

### 9. Power to Evolve System Structure

**The authority and capability to change how systems are organised**

- Microservices evolution and decomposition strategies
- Adaptive architectures that can reshape themselves
- Cloud elasticity and auto-scaling capabilities
- Platform teams with mandate to evolve infrastructure

### 8. Rules and Policies

**The formal and informal rules that govern system behaviour**

- Security policies and compliance constraints
- Service-level agreements and error budgets  
- Architectural governance and decision records
- Change management and deployment policies

### 7. Information Flows and Feedback Loops

**How information moves through the system and creates learning**

- Observability platforms and distributed tracing
- Comprehensive telemetry, logging, and monitoring
- Real-time dashboards and alerting systems
- Feedback from production to development teams

### 6. System Structure and Relationships

**The physical and logical architecture of your systems**

- System topology and service boundaries
- Data pipelines and event streaming architectures
- Integration patterns and API design
- Service mesh and infrastructure layout

### 5. Automated Controls and Circuit Breakers

**The mechanisms that regulate system behaviour automatically**

- Automated circuit breakers and bulkhead patterns
- Throttling mechanisms and rate limiting
- Error handling and retry policies
- Failover systems and chaos engineering

### 4. Material Flows and Scaling

**How requests, data, and load move through your system**

- Auto-scaling policies and triggers
- Event-driven propagation patterns
- Demand amplification and load balancing
- Capacity planning and resource allocation

### 3. Regulating Mechanisms

**The buffers and controls that manage system stability**

- Queue depth management and backpressure
- Caching strategies and data locality
- Message buffers and batch processing
- Connection pooling and resource limits

### 2. Material Elements

**The fundamental components and their characteristics**

- Transaction latency optimisation
- Batch processing windows and scheduling
- Settlement cycles and consistency models
- Database performance and indexing

### 1. Constants and Parameters *(Lowest Leverage)*

**The numbers and settings you can adjust**

- API rate limits and timeout configurations
- Retry attempt counts and backoff strategies  
- Connection pool sizes and buffer limits
- Cache expiry times and refresh intervals

---

## Practical Applications

### Focus Your Architectural Efforts

Instead of spending weeks tweaking timeout values, consider: Could you change how the team thinks about system boundaries? Could you introduce better observability to create faster feedback loops?

### Influence Strategy

When presenting to leadership, lead with paradigm shifts and cultural changes. These create the most sustainable improvements and demonstrate strategic thinking.

### Technical Debt Prioritisation

Frame technical debt discussions in terms of leverage. Fixing architectural principles (high leverage) vs patching individual services (low leverage) becomes a clearer conversation.

### Team Development

Invest in changing how your team thinks about systems, not just what tools they use. The mindset shift creates lasting impact across all future decisions.

## Why This Framework Matters

Traditional approaches often focus on the visible, technical elements - the parameters and configurations at the bottom of the hierarchy. But these provide the least leverage for change.

The most effective system architects operate at the paradigm level, asking questions like:

- How do we fundamentally think about system resilience?
- What should our relationship be between speed and stability?  
- How do we balance autonomous teams with system coherence?

These questions reshape everything that follows.

## Conclusion

Systems thinking reminds us that **where** you intervene in a system is often more important than **how** you intervene. By focusing your architectural efforts on higher leverage points - particularly paradigms and culture - you can create more significant, lasting change with less effort.

The next time you're faced with an architectural challenge, ask yourself: Am I working on parameters, or am I working on paradigms? The answer might transform how you approach the problem entirely.

---

## The original 12 leverage points as described by Dana Meadows

12. Constants, parameters (numbers, subsidies, taxes, standards)
	•	Tweaking numbers rarely shifts the system’s behaviour in a fundamental way.
	•	Example: changing tax rates or setting limits — small adjustments at best.

11. Sizes of buffers and stocks relative to flows
	•	Changing physical capacities (like inventory or reserves) alters how stable or resilient a system is.
	•	Example: a dam’s size relative to water inflow.

10. Strength of negative feedback loops
	•	How well the system can self-correct when it drifts from a desired state.
	•	Example: thermostat responsiveness.

9. Gain of positive feedback loops
	•	Controlling reinforcing loops that create runaway growth or decline.
	•	Example: curbing interest compounding or disease spread.

8. Structure of information flows
	•	Who has access to information and how quickly they get it changes decisions and outcomes.
	•	Example: publishing pollution levels so communities can respond.

7. Rules of the system
	•	Formal and informal rules (incentives, punishments, boundaries) shape behaviour.
	•	Example: laws, contracts, property rights.

6. Power to change the rules
	•	Who gets to set, enforce, and change the rules has more leverage than the rules themselves.
	•	Example: a parliament, regulator, or board of directors.

5. Goals of the system
	•	The purpose the system is organised around. Change the goal, and everything else shifts.
	•	Example: from maximising profit → maximising wellbeing.

4. Paradigms (mindsets, worldviews)
	•	The underlying assumptions and beliefs from which system goals and rules arise.
	•	Example: “Growth is good” vs. “Enough is enough.”

3. Ability to transcend paradigms
	•	Seeing paradigms as models, not truths, and remaining flexible about which to use.
	•	Example: blending economic, ecological, and cultural perspectives.

2. –
	•	(Some lists compress 2 & 3 into one, since both concern paradigm flexibility.)

1. Transcending paradigms completely
	•	The deepest leverage: recognising that no paradigm is the truth, staying unattached, and free to create new ways of seeing.
	•	Example: Zen-like awareness that allows radical system redesign.

⸻

The essence: lower leverage points (12–9) adjust mechanics, mid-level (8–6) alter structure, high leverage (5–1) reshape intent and worldview.