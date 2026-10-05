---
title: "The Red Queen"
summary: "Running faster just to stand still"
description: "Expectations, Tooling, Risk and Threats are all accelerating. An engineer has to accelerate just to stand still."
draft: true
tags: ["agent-engineering", "generative-ai", "cyber", "risks"]
categories: ["engineering"]
author: "Gary Thomas"
date: 2026-10-05
cover:
  image: "the_red_queen.svg"
---

# The Req Queen
## The Absurdist Race

In Lewis Carroll's Through the Looking-Glass (1871), Alice takes the Red Queen’s hand and finds herself in a breathless, frantic sprint across the surreal chessboard landscape. Despite running at top speed until she is exhausted, the surrounding trees and scenery never change position.

When they finally stop, Alice finds herself resting under the exact same tree where they began. When she expresses bewilderment—noting that in her world, running fast gets you somewhere else—the Red Queen explains the logic of Looking-Glass land: here, you have to run as fast as you can just to stay in the same place. If you want to actually get somewhere else, you must run at least twice as fast as that.

## The Modern Day Parallel

I was listening to an economics blog post which quoted this same reference, I have a number of other references to the same absurdist scenario recently and it resonated with me and my day to day experience as the I think we are experiencing the same phenomena in Software Engineering and Cybersecurity?

This scene gave rise to several influential cultural and scientific concepts:

⚬ The Red Queen Hypothesis (Evolutionary Biology): Proposed by Leigh Van Valen in 1973, this principle posits that organisms must constantly adapt, evolve, and proliferate simply to survive against ever-evolving opposing organisms (such as predators, parasites, or competitors) in a dynamic ecosystem. Stasis means extinction.
⚬ Economic and Business Competition: Often used to describe markets where companies must relentlessly innovate, spend on R&D, and lower margins just to maintain their existing market share against rivals doing the exact same thing.
⚬ Technological and Societal "Treadmills": In sociology and philosophy, it serves as a metaphor for the relentless pace of modern life—working longer hours or adopting faster tools merely to keep up with escalating baselines rather than getting ahead.

AI tooling and cyber threats are both running on the same treadmill, just from opposite sides.

The asymmetry is where things start to get difficult. Defenders and attackers both get faster with AI, but the gains aren't symmetric. Attackers need one success and carry no compliance overhead. Defenders in a regulated environment have to move fast and demonstrate control: evidence for CPS 234, audit trails, change governance. 

Every acceleration on the delivery side increases the volume of change that has to be assured. If assurance doesn't scale at the same rate, you're not standing still, you're falling behind while feeling busy. Even though you may have significant productivity improvements this is the new normal, you are expected and required to move ever faster.

Where the Red Queen's second clause matters. "Twice as fast to get somewhere else" is the useful line. Running harder at the same things (more tickets closed, more code generated, more patches applied) just holds position. Getting somewhere requires changing what you're running on:

** Shifting controls left and making them declarative. Policy-as-code (OPA, Cedar) means a new service inherits enforcement rather than needing a review cycle. The control scales with the platform, not with headcount.
** Reducing the surface rather than defending it faster. Fewer bespoke paths, standardised golden paths, smaller dependency footprints. Every thing you don't have is a thing you don't have to patch at AI-accelerated disclosure speeds.
** Automating assurance, not just delivery. Continuous evidence generation so audit readiness is a by-product of the pipeline rather than a periodic scramble.
** Treating AI-generated code as higher-volume, lower-provenance input. The bottleneck moves from writing to verifying, so investment in tests, contract checks, and review tooling has to move with it.

The treadmill also implies a hidden, or actually, not so hidden cognitive load. The sociological version of the metaphor, escalating baselines, shows up as teams adopting each new tool to keep pace with expectations that the tool itself raised! 

Productivity gains get absorbed into higher throughput KPIs rather than into slack for design thinking or additional time to perform system hardening. 

Which raises the question: `what is the organisation choosing to spend the AI dividend on? `

If the answer is "more features," the treadmill speeds up. If some of it is deliberately reinvested in resilience and simplification, you may get some real benefit. But, this is a brave call in a competitive and rapidly changing landscape.

A useful test that can be applied to any initiative: does it compound, or does it merely sustain? Running to stay in place is sometimes unavoidable (patching is patching), but a healthy portfolio should have a visible share of work that changes the terms of the race rather than just the pace.

The other question, that has not yet been addressed is how much do we trust the agents themselves to perform the resilience, patching, vulnerability fixes, not just the identification?

## The Core Premise: Where Does Value Actually Come From?
When generation is cheap and everyone is accelerating, output volume ceases to be a competitive advantage—it becomes table stakes.

If you use AI solely to produce more code, tickets, and features, you haven’t created value; you’ve just increased the velocity of your treadmill and the volume of assurance required.

Value doesn't come from running faster; value comes from changing what you are running on:

### Cycle Time to Verified Truth (Latency over Throughput)
Value isn't lines of code or closed tickets—it is how fast an idea, hypothesis, or security patch safely reaches production and validates itself. Compressing feedback loops from weeks to minutes is compounding value; generating 500 lines of unverified code in 10 seconds is just operational inventory.

### Subtractive Engineering (Reducing Surface Area)
Because AI makes creation friction-free, complexity gets cheaper to build and exponentially more expensive to maintain and assure. True economic value comes from using AI to delete, consolidate, and standardise—reducing the surface area that defenders must assure at AI-accelerated disclosure speeds.

### Assurance Decoupled from Headcount
In regulated environments (e.g., CPS 234), delivery without assurance is un-deployable debt. Value comes from turning governance from an intermittent human tollbooth into continuous, automated platform telemetry.

## Strategic Capital Allocation ("The AI Dividend")
Value comes from the deliberate discipline of not pouring 100% of productivity gains back into feature roadmaps. Capturing real enterprise value requires capturing "slack" to rethink architectures, harden systems, and eliminate legacy drags.

## The Options: Four Paths Organizations Take
When faced with the Red Queen dynamic, engineering organizations typically pick (or drift into) one of four operating modes:

                          ▲ HIGH
                          │
         [ Option 2 ]     │     [ Option 3 & 4 ]
       DEFENSIVE MOAT     │    PLATFORM LEVERAGE &
    (Freeze & Gatekeep)   │    AUTONOMOUS ASSURANCE
                          │
  GOVERNANCE & ASSURANCE  │
                          │
                          │         [ Option 1 ]
                          │       THROUGHPUT TRAP
                          │     (Feature Churn & Burn)
                          │
                          └────────────────────────► HIGH
                               VELOCITY / ADOPTION
### Option 1: The Throughput Trap (Velocity without Direction)

What it looks like: Reinvesting all AI efficiency gains into sprint velocity KPIs, backlog burn-down, and more features.
The outcome: Complexity explodes, review queues become catastrophic bottlenecks, engineers burn out from cognitive thrash, and assurance debt mounts.

### Option 2: The Defensive Moat (Bunker Down & Gatekeep)

What it looks like: Applying pre-AI compliance frameworks, heavier manual review gates, and risk committee sign-offs to slow down generative tooling.
The outcome: Paralysis. Shadow AI sprouts up, developers find workarounds, and while your defenders are frozen in review, attackers continue to accelerate.

### Option 3: Platform Refactoring (Changing the Terrain)

What it looks like: Deploying the AI dividend to modernize legacy platforms, mandate declarative golden paths, and shift controls left (policy-as-code).
The outcome: The platform absorbs complexity so the individual engineer doesn't have to. Assurance scales with platform adoption, not headcount.

### Option 4: Graduated Autonomous Remediation (Changing the Runner)

What it looks like: Moving AI agents from passive "spotters" (generating alerts and ticket backlogs) to active, bounded "actors" (automated dependency patches, synthetic regression repair, drift remediation).
The outcome: Closes the asymmetry gap against external threats by matching automated attack speeds with automated defensive responses.
How to Make Decisions: A Decision Framework
To avoid getting trapped on the treadmill, leaders and teams need explicit heuristics:

1. The Compounding Test
"Does this initiative compound our capabilities, or merely sustain our current position?"

Sustaining (Treadmill): Routine patching, triage, manually reviewing boilerplate PRs, meeting audit deadlines via manual spreadsheets.
Compounding (Escape Velocity): Declarative policy enforcement (OPA/Cedar), automated compliance evidence pipelines, self-service golden paths, deleting 20,000 lines of obsolete glue code.
The Rule: Mandate a non-negotiable allocation (e.g., 30–40%) of engineering capacity specifically to compounding initiatives.
2. The Bottleneck / Theory of Constraints Test
"Are we optimizing the step that is actually holding up delivery and safety?"

If code generation is 5x faster, spending more effort optimizing developer prompt tooling yields zero enterprise value if security review or staging assurance takes 3 weeks.
The Rule: Point AI leverage at the current constraint—verification, synthetic test generation, contract checking, or audit readiness.
3. The Net-Complexity Heuristic
"Did this change reduce our operational footprint or expand it?"

When evaluating new architectures or AI-assisted initiatives, measure not just feature delivery, but net dependencies added, runtime abstractions created, and long-term assurance cost.
4. The Agency & Trust Matrix (Deciding Agent Autonomy)
How do we decide when to trust agents to fix and remediate, not just find problems? Use a graduated blast-radius model:

Level	Role	Action	Verification
L1: Informational	Passive Advisor	Flags vulnerability / drift in CI	Human triage & human fix
L2: Suggestive	Drafter	Creates PR with targeted test suite	Human review & merge
L3: Bounded Auto	Operator (Pre-Prod)	Auto-patches non-breaking dependencies & tests in sandbox	Automated contract verification
L4: Autonomous	Self-Healing (Prod)	Bounded rollback, auto-isolation, deterministic policy fix	Telemetry canary + audit event log
