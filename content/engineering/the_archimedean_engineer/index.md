---
title: "The Archimedean Engineer"
summary: "Using AI Tools as a Lever"
description: "How to provide structure to the leverage that AI engineering tools provide to the"
draft: true
tags: ["kiro", "agent", "gemini", "claude", "AWS]
categories: ["engineering"]
author: "Gary Thomas"
date: 2026-08-28
---

# The Archimedean Engineer
## Engineering in the Age of AI

> *“Give me a place to stand, and with a lever long enough I can move the world.”*  
> — Traditionally attributed to Archimedes

We are entering a different era of software engineering.

AI can write code. It can generate tests, explain unfamiliar systems, refactor modules, explore alternatives, create documentation and automate enormous amounts of mechanical work.

The question is no longer:

**“Can AI write software?”**

It clearly can.

The more important question is:

**“What kind of engineering organisation do we need to become if we want to safely exploit that capability?”**

And I believe the answer is surprisingly simple.

**AI is an accelerator, not an anchor.**

It amplifies whatever engineering system we put underneath it.

If our architecture is clear, our specifications are precise, our tests are trustworthy and our feedback loops are fast, AI gives us extraordinary leverage.

If our requirements are vague, our architecture is coupled, our tests are unreliable and our feedback loops are slow, AI doesn't fix those problems.

**It makes them bigger, faster.**

That is the opportunity—and the challenge.

---

# 1. The Archimedean Model

Think about the problem through Archimedes' idea of leverage.

We have four things:

**The Force — Human Intent**

The engineer understands the customer, the business, the domain, the risks and the trade-offs.

**The Lever — AI**

AI provides enormous mechanical leverage. It can translate intent into code, tests, transformations, documentation and alternatives at a speed no individual engineer can match manually.

**The Fulcrum — Engineering Discipline**

This is where our engineering practices matter:

- Clear specifications
- Automated tests
- Strong invariants
- Modular architecture
- Explicit interfaces
- Continuous integration
- Fast feedback
- Continuous refactoring
- Security and quality controls

**The Load — The Problem**

The complexity of the systems we need to build and change.

The better the fulcrum, the more leverage we can safely apply.

And this leads to the central idea of this talk:

> **AI gives us a longer lever. Our job is to build a stronger fulcrum.**

---

# 2. Specification Before Generation

The first change is perhaps the most important:

**We need to become better at specifying software before asking AI to generate it.**

AI is extraordinarily good at producing an answer.

That does not mean it knows whether the answer is the right one.

The human must establish:

- What problem are we solving?
- What are the invariants?
- What are the business rules?
- What are the edge cases?
- What must never happen?
- What does success look like?

Tests and executable specifications become more important—not less.

They give AI something objective to work against.

Instead of:

> “Build me a customer onboarding service.”

We should increasingly be able to say:

> “Here is the contract. Here are the invariants. Here are the acceptance criteria. Here are the tests. Implement the behaviour.”

That is a fundamentally different relationship with AI.

**We are not asking AI to invent the specification.**

We are giving it a constrained problem and asking it to provide the implementation.

The test harness becomes an anchor.

---

# 3. Simplicity Becomes a Superpower

The second change is architectural.

AI gives us an extraordinary ability to generate code.

That creates a new risk:

**The cost of creating complexity is falling.**

We can create another abstraction.

Another wrapper.

Another framework.

Another helper.

Another layer.

Another 1,000-line generated component.

And because AI produced it in seconds, it is dangerously easy to accept it.

This means simplicity becomes more important, not less.

Small modules.

Clear responsibilities.

Explicit interfaces.

Well-defined boundaries.

Pure functions where appropriate.

Minimal dependencies.

Simple designs.

**The objective isn't maximum code generation.**

It is maximum useful change per unit of complexity.

AI should help us simplify systems—not merely add to them.

---

# 4. Feedback Loops Become Our Competitive Advantage

AI can generate software extremely quickly.

Therefore our limiting factor increasingly becomes:

**How quickly can we determine whether what it generated is correct?**

That makes feedback loops a strategic capability.

A developer should be able to make a change and receive meaningful feedback in seconds where practical:

- Formatting
- Linting
- Type checking
- Unit tests
- Contract validation
- Static analysis
- Local builds

Broader integration, security and system tests can follow in the CI pipeline.

The principle is simple:

> **The faster we can detect a bad change, the more safely we can make changes.**

AI changes the economics of development.

Generated code should become disposable.

Generate.

Verify.

Keep it—or throw it away.

Then try again.

We don't need to become precious about AI-generated code.

**We need to become ruthless about quality.**

---

# 5. Humans Become More Important—Not Less

There is a temptation to describe AI as the replacement for the developer.

I think that misses the opportunity.

AI is exceptionally good at mechanical work.

Humans remain accountable for intent.

The human owns:

- The problem
- The domain
- The architecture
- The boundaries
- The risks
- The security model
- The trade-offs
- The consequences

AI can be the driver.

But the engineer remains the navigator.

And there is an important rule here:

> **AI can generate the implementation. It cannot outsource accountability.**

If AI creates a change, we still own that change.

We need to understand its behaviour, its implications and its failure modes.

The goal isn't to remove humans from the engineering loop.

It is to remove humans from unnecessary mechanical effort so that they can spend more time on the things that actually require engineering judgement.

---

# 6. Refactoring Becomes Continuous

There is another consequence of cheap code generation.

**Code becomes abundant.**

And abundant code becomes clutter.

AI makes it incredibly easy to add functionality.

It also makes it incredibly easy to remove duplication, simplify designs and refactor legacy code.

We should exploit both.

A healthy AI-enabled engineering culture should regularly ask:

> **Can we make this simpler?**

Not:

> “How much more can we build?”

But:

> “What can we delete?”

> “What can we consolidate?”

> “What abstraction is no longer earning its keep?”

> “Can we express this behaviour more clearly?”

AI should become one of our most powerful refactoring tools.

**The measure of engineering productivity should not be lines of code generated.**

Sometimes the highest-value AI contribution is the code that disappears.

---

# 7. Discipline Before Autonomy

This brings us to the biggest organisational change.

Everyone wants autonomous agents.

Agents that understand a ticket, change the code, write the tests, raise the pull request and move on to the next task.

That future is coming.

But autonomy magnifies the quality of the system underneath it.

If our architecture is inconsistent, our specifications vague and our tests unreliable, giving an agent more autonomy simply allows it to make more changes before anyone notices.

So we should think about autonomy as something we **earn**.

First:

**Good engineering practices.**

Then:

**Automation.**

Then:

**AI assistance.**

Then:

**Higher levels of AI autonomy.**

The stronger our foundations, the further we can safely push autonomy.

---

# The Opportunity

This is not an argument for slowing down.

It is the opposite.

AI gives us an opportunity to dramatically increase the rate at which we can transform our systems.

But to capture that opportunity, we need to change the way we engineer.

We need:

**Smaller changes.**

**Clearer specifications.**

**Stronger contracts.**

**Better tests.**

**Simpler architectures.**

**Faster feedback.**

**Continuous refactoring.**

**Greater automation.**

And above all:

**Higher engineering standards.**

---

# The New Engineering Loop

The old model was often:

> Understand → Design → Build → Test → Deploy

The AI-enabled model should become:

> **Specify → Generate → Verify → Refine → Repeat**

And the cycle should become dramatically shorter.

We don't need AI to produce perfect code on the first attempt.

We need an engineering system that makes imperfect output cheap to detect and cheap to replace.

That is a profound shift.

---

# The Unified Axiom

AI is perhaps the most powerful software engineering lever we have ever been given.

But a longer lever doesn't automatically move a heavier load.

**It demands a better fulcrum.**

Our engineering discipline is that fulcrum.

Our architecture provides the boundaries.

Our tests provide the constraints.

Our feedback loops provide the control system.

And our engineers provide the intent, judgement and accountability.

So the challenge for us isn't:

**“How do we stop AI from writing bad code?”**

It is:

**“How do we build an engineering system in which AI can safely produce enormous amounts of useful change?”**

That is a much more exciting question.

Because if we get this right, we don't simply write software faster.

We can change systems faster.

We can modernise legacy platforms faster.

We can experiment faster.

We can learn faster.

We can respond to customers faster.

We can reduce the mechanical burden on engineers.

And we can spend more of our time solving the problems that actually matter.

> **AI is the lever.**
>
> **Engineering discipline is the fulcrum.**
>
> **Human intent provides the direction.**
>
> **And the opportunity is to move the world of software further and faster than we have ever been able to before.**