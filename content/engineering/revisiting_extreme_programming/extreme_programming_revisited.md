---
title: "Extreme Programming Revisited"
description: "An overview of Extreme Programming (XP) and why it is still important in a world of vibe coding."
draft: true
ShowToc: false
TocOpen: false
author: "Gary Thomas"
date: 2025-05-19
image: "/engineering/revisiting_extreme_programming/xp-workflow.svg"
---

## Introduction

Extreme Programming ([XP](https://www.extremeprogramming.org/)) is a software development methodology that emphasizes the importance of delivering working software to customers as quickly as possible.

I was struck by what seemed to be some comments on AI coding assistance that highlighted a number of key findings about the approaches that engineers found more successful:
* Prompt using test cases or examples
* Work in small steps
* Test continuously
* Review code and refactor continuously
* Commit after every small step when the tests pass
* Sync with the trunk branch often

It appears that a lot of the things that are attributing to LLMs and MCP are actually also about improving the approach to engineering. I am not saying that having a coding colleague as productive and knowledgeable as an AI Agent is not going to make a significant difference, but just like in all teams we need to work out how best to interact to get the highest level of productivity.

Looking at the above list there are a couple of things that leap out, which seem to align with established thinking - Test Driven Development(TDD), Specification by Example and Continuous Integration.

Maybe what we are seeing though is that AI generated code is moving us closer to a pure form of XP. Where the secret as Michael Fowler pointed out [here](https://martinfowler.com/bliki/SpecificationByExample.html) is that in XP rather than just doing things once we were always doing things twice (writing the test and writing the code). With AI we can do it once, but we still need to specify the test to ensure what was generated is what we want. (I was going to say 'we' making the Agent part of the team, but I am not sure we can assign sentient behaviour quite yet).

## Key Principles

![Workflow](/engineering/revisiting_extreme_programming/xp-workflow.svg)


### Customer Collaboration

### Feedback

### Simplicity

### Continuous Improvement

### Teamwork

There are still multiple members to the team, but the more we work with AI Agents the more we need to know how to interact with them. The size of the context window is ever increasing, but we still need to be able to break down the problem into smaller steps and also ensure that what we ask them to do is clear and unambiguous to get the best results.