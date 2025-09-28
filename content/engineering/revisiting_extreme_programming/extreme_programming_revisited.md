---
title: "Extreme Programming Revisited"
description: "An overview of Extreme Programming (XP) and why it is still important in a world of AI-assisted development."
draft: false
ShowToc: false
TocOpen: false
author: "Gary Thomas"
tags: ["extreme-programming", "XP", "agentic-coding", "AI-assisted-coding", "TDD", "Specification-by-Example", "Continuous-Integration", "DORA"]
categories: ["engineering", "AI"]
date: 2025-09-20
image: "/engineering/revisiting_extreme_programming/revisiting_extreme_programming.svg"
---

# Introduction

Extreme Programming has been declared dead more times than I've sat through presentations about "digital transformation initiatives." Yet here we are again, breathlessly rediscovering that writing tests and integrating frequently might actually be quite sensible. Who could have predicted such a thing? 

I should state before I continue that I am not an XP zealot. I've never been fond of the term "Extreme Programming," nor of prescriptive adoption of practices just because we’re told that’s the way. As with all things, it’s the principles, and why they matter, that lead to better outcomes.

Recent findings about successful AI-assisted development read like a greatest hits collection from 1999. Apparently, the secret sauce includes:

* Prompting with test cases or examples
* Working in small steps
* Testing continuously
* Reviewing code and refactoring continuously
* Committing after every small step when the tests pass
* Syncing with the trunk branch often

Revolutionary stuff. One might almost think we'd discovered these principles before, perhaps around the time we were all worried about Y2K and installing Windows ME.

These practices look suspiciously like some of the key capabilities identified by [DORA](https://dora.dev/), and bear an uncanny resemblance to **Test-Driven Development (TDD)**, **Specification by Example**, and **Continuous Integration**. It's almost as if we've been here before.

Perhaps what we're witnessing is AI dragging us — kicking and screaming — back to a **purer form of XP**, or at least some of the associated principles. As Martin Fowler pointed out [here](https://martinfowler.com/bliki/SpecificationByExample.html), the secret of XP was doing things twice: writing the test and writing the code. With AI, we can do it once, but we still need to specify the test to ensure what was generated bears some resemblance to what we actually wanted, rather than what we accidentally asked for.

The irony is that artificial intelligence might finally force us to follow the blindingly obvious advice we've been cheerfully ignoring since 1999. Rather than making XP obsolete, AI-assisted development provides a unique opportunity to return to the purest form of XP — assuming we can resist the urge to overcomplicate it with blockchain-flavoured DevOps pipelines, or whatever we’re calling unnecessary complexity this week.

---

# Key Principles

## Customer Collaboration

In the halcyon days of waterfall development, customers were rather like visiting dignitaries. They appeared at the beginning to issue proclamations about requirements, vanished for months whilst we built whatever we thought they'd said, and then reappeared at the end to express surprise that we'd built something entirely different. The feedback loop was roughly equivalent to sending messages by carrier pigeon, which is still faster than some of the change request processes I've seen in Australia.

Modern product-centric delivery treats customer collaboration as a continuous conversation rather than a scheduled meeting. Instead of managing scope in a project (and watching it creep like ivy up a garden wall), we manage outcomes in a product:

* **Ongoing Engagement**: Customers actually stick around throughout development, rather than disappearing like witnesses in a particularly dull crime drama
* **Shared Product Vision**: Teams rally around a product roadmap instead of a Gantt chart that's been out of date since the moment it was produced
* **Feedback Loops**: Customer input gets integrated into each iteration, rather than being filed under "post-launch enhancement requests"
* **Value Focus**: Engineering decisions are guided by actual customer value, not the whims of whoever shouts loudest in the planning meeting

AI-assisted development amplifies this by enabling rapid prototyping and faster iterations. When you can knock up a working prototype in an afternoon rather than a fortnight, it becomes considerably easier to show customers what you're thinking, and discover whether they're thinking the same thing. The essence remains pure XP: the best measure of progress is working software in the hands of engaged customers, not comprehensive documentation gathering dust in SharePoint.

---

## Feedback

Traditional development treated feedback like a scheduled maintenance event, something that happened at prescribed intervals, usually too late to be of much use. XP transforms feedback from a calendar appointment into a continuous, multi-layered conversation with your code.

In the old world, feedback arrived with the reliability of British trains and roughly the same level of user satisfaction. You'd spend months building something, present it to users during UAT, and then spend more months fixing everything they politely suggested was "not quite what we had in mind," or not so politely escalated to the nearest General Manager.

XP builds feedback into every breath of the development process:

* **Automated Testing**: Every line of code gets a continuous health check, like having a pair programmer who's actually right about everything
* **Pair Programming**: Real-time code review happens as you work, catching issues before they metastasise into "architectural decisions"
* **Continuous Integration**: Every commit gets integrated and tested, ensuring the system works as a coherent whole rather than a collection of individually brilliant components that despise each other
* **Short Iterations**: Features get delivered in testable increments, allowing for frequent course corrections before you've sailed too far off the edge of the map

Here's the delightful bit with AI-assisted development: AI can generate catastrophically wrong code at a rate that would make even the most optimistic junior developer weep with envy. It's like having a colleague who never gets tired, never questions requirements, and has absolutely no sense of self-preservation when it comes to production deployments.

This means your feedback loops had better be fast, or you'll soon be explaining to stakeholders why the AI decided that deleting all customer data was "probably what you meant."

* **AI-Generated Code Review**: Humans must critically evaluate AI suggestions with the suspicious eye of someone who's been promised "this will only take five minutes" one too many times
* **Test-First Development**: Writing tests before implementation creates clear success criteria for both humans and AI
* **Runtime Monitoring**: Observability tools provide feedback on how AI-generated code performs in production; the feedback loop should not end; you need visibility into what is happening in your code

The most effective feedback leads to immediate action. Whether it's a failing test, a code review comment, or a production alert that makes your phone buzz insistently, XP values systems that turn feedback into improvement without the traditional without the traditional six-week change-control board review.

---

## Simplicity

The principle of "do the simplest thing that could possibly work" suddenly becomes rather urgent when your AI pair programmer has the architectural subtlety of a blunt instrument. Agents need very clear direction and prompting to produce the output you require.

AI agents are often surprisingly good at generating straightforward, concise solutions when properly directed. They can act like that rare consultant who actually answers the question you asked rather than the one they wanted you to ask. The goal remains avoiding over-engineering and building only what's required for the current iteration — not what might possibly be needed if the business suddenly decides to pivot into cryptocurrency mining.

---

## Continuous Improvement

The XP practice of **refactoring** has always been about continuous improvement, the gentle art of making code less embarrassing without changing what it actually does. With AI, this practice gets amplified.

An AI agent can act as a tireless refactoring engine, continuously suggesting small improvements to the codebase with the persistence of a junior developer who's just discovered design patterns. This frees the human to focus on higher-level architectural challenges rather than getting bogged down in the sort of boilerplate code that makes experienced developers question their life choices.

The human validates proposed refactoring to ensure it aligns with the system's overall architecture and doesn't accidentally introduce that special brand of cleverness that makes future maintainers curse your name. It's a symbiotic relationship: the AI tirelessly fiddles with the small stuff whilst the human keeps an eye on the bigger picture.

---

## Teamwork

XP's focus on teamwork hasn't been made redundant by AI; it's been clarified. The "pair" is now a human and an enthusiastic assistant that never needs coffee breaks, never complains about your code or coding ability, and hasn't yet learned to passive-aggressively update JIRA tickets.

It's rather like working with an intern who's read every programming book ever written but still needs supervision when using scissors. The AI doesn't attend stand-ups, doesn't argue about story points, and hasn't yet learned to explain why a two-point story became a five-day odyssey through dependency hell. Give it time — someone’s probably working on that feature.

The human's role shifts from typing to thinking — from "how do I implement this algorithm?" to "should this algorithm exist at all?"

The best results come from treating AI as a powerful tool to be used collaboratively, not as a replacement for the sort of human interaction that prevents projects from disappearing into architectural rabbit holes.

---

## Trunk-Based Development and Continuous QA

These practices are the yin and yang of XP: **trunk-based development** provides the rhythm of frequent integration, whilst **continuous QA** ensures that every integration doesn't accidentally set everything on fire. When AI agents are generating large amounts of code, this combination becomes the difference between controlled progress and automated chaos.

### Trunk-Based Development

XP has always emphasised integrating with the trunk frequently, avoiding long-lived branches that inevitably become archaeological digs of abandoned good intentions. With AI-generated code, this discipline becomes even more critical: the risk of drift multiplies when an agent can generate more code in ten minutes than a human might write in a day.

* **Small Steps**: Encourage both developers and AI agents to work in digestible increments, committing frequently rather than attempting to solve all features in a single commit
* **Feature Flags**: Use feature flags to safely integrate incomplete features without turning the trunk into a dumping ground that can never safely be released
* **Human + Agent Collaboration**: Treat the AI as a pair programmer whose enthusiasm needs channelling through the team's standards and architectural vision
* **Governance**: Frequent integration keeps the whole system visible, helping detect when AI output has wandered into creative territory best left unexplored

### Continuous QA

Continuous QA extends XP's practice of continuous testing into a comprehensive safety net — which becomes rather essential when your AI colleague generates code with all the caution of someone who's never had to field a 3 AM support call.

* **Tests as Specifications**: Writing tests first gives the AI a clear contract to code against, reducing the likelihood of creative interpretations that seemed reasonable at the time
* **AI-Augmented Testing**: AI can generate additional edge-case tests and fuzzing scenarios, expanding coverage beyond what humans might anticipate or consider
* **Pipeline as Gatekeeper**: Every commit flows through a robust CI/CD pipeline that validates thoroughly and quickly (being able to commit frequently depends on a build pipeline that runs in minutes)
* **Runtime Validation**: Continuous QA includes observability and monitoring in production, ensuring that AI-generated changes are not just syntactically valid but operationally correct

Together, trunk-based development and continuous QA maintain the pace of AI-assisted development whilst preserving the discipline that prevents rapid progress from becoming rapid disaster.

---

# Guardrails and Patterns

Whilst trunk-based development and continuous QA provide excellent feedback loops, they don't automatically ensure that AI-assisted development stays within the bounds of sensible engineering practice. **Guardrails and patterns** act as the architectural conscience of the process, ensuring that both human and agent contributions maintain some resemblance to professional software development.

## Why They Matter More Than Ever

AI agents can produce perfectly functional code that passes all tests whilst simultaneously violating every architectural principle you hold dear. Without explicit boundaries, it's remarkably easy for inconsistencies, security vulnerabilities, or anti-patterns to creep in like weeds in an otherwise respectable garden.

In the old days, we absorbed standards and patterns through osmosis — pairing sessions, code reviews, and the occasional educational correction from a senior developer. Now we need to bottle up this institutional knowledge explicitly: ADRs, prompts, linting rules, and other forms of digital wisdom that prevent our silicon teammates from going off course.

## How to Apply Them

* **Architecture Decision Records (ADRs)**: Document key decisions so that both AI agents and humans work with the same architectural intent
* **Curated Documentation Awareness**: Provide AI tools with access to reference architectures and coding standards, though be prepared for them to follow these literally
* **Linting and Policy as Code**: Enforce standards automatically through static analysis
* **Secure Defaults and Templates**: Supply compliant scaffolds so generated code begins with sensible patterns rather than whatever seemed like a good idea at the time
* **Prompting Standards**: Encourage developers to specify required patterns in their prompts (e.g., "implement using repository pattern")
* **Automated Fitness Functions**: Use architectural fitness functions to continuously validate that the system maintains its intended design

## Relationship to XP Values

In traditional XP, refactoring and pair programming spread good practices organically through the team. In AI-assisted XP, we maintain those same values by codifying sensible rules into automated guardrails. This ensures that the velocity gained from AI assistance doesn't come at the cost of architectural sanity or the sort of technical debt that makes grown developers weep.

This organic spread of knowledge now needs to be codified and made explicit, rather than simply hoped for.

---

# Conclusion

The irony is that we needed artificial intelligence to finally convince us to follow the obvious advice we've been cheerfully ignoring since 1999.

AI hasn't made XP obsolete; it's made XP urgent. When you can generate code faster than you can think about whether you should, the discipline of small steps, continuous feedback, and ruthless simplicity becomes the difference between progress and pandemonium.

Perhaps there's something poetic about needing machines to teach us how to be sensible about building software. Or perhaps it's just another data point in our industry's impressively consistent ability to overcomplicate simple problems, forget hard-won lessons, and then rediscover them with the enthusiasm of someone who thinks they've just invented fire.

The fundamentals haven't changed: deliver working software frequently, get feedback early, keep it simple, and don't let perfect be the enemy of good enough. The tools have simply become more powerful and, occasionally, more creative in their interpretation of our instructions.

Progress, I suppose, comes in many forms — even when it looks suspiciously like reinventing the past.