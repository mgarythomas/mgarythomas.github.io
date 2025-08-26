---
title: "Architectural Options: Managing Change and Uncertainty for Stakeholders"
summary: "How an architecture provides options for stakeholders"
description: "How architects provide stakeholders with strategic options to manage uncertainty, defer decisions, and align architecture with evolving business needs."
draft: false
tags: ["options", "architecture", "volatility", "risk"]
categories: ["architecture"]
author: "Gary Thomas"
date: 2025-04-26
image: "/architecture/architecture-options/options-architecture-share.png"
---

In any technology project, uncertainty is inevitable. New requirements emerge, priorities shift, and unforeseen challenges arise. This reality became particularly clear to me working in financial services, where architectural decisions must navigate not just technical uncertainty, but also customer expectations, regulatory changes, market volatility, and evolving security threats.

In this highly-regulated environment, the concept of architectural optionality isn't just theoretical—it's essential for survival. A trading system that can't adapt to new regulations, a settlement system that can't handle volume spikes, or a security framework that can't evolve with emerging threats becomes a business liability.

To address this, architects must design systems that provide optionality — enabling stakeholders to defer decisions where possible, manage evolving risks, and preserve flexibility without committing prematurely.

---

## How Do We Provide Optionality for Our Stakeholders?

Anyone who has worked on technology projects will know that, at the beginning of a project, certain elements remain uncertain, or new requirements and changes of direction may arise over time.

This is why presenting options during the development of architecture and in engagement with various stakeholders is crucial. This concept is widely recognised within the architecture community; Gregor Hohpe and Martin Fowler have discussed the importance of offering options in architecture [here](https://martinfowler.com/articles/architect-elevator.html#SellArchitectureOptions).

From my perspective, the concept of providing options in architecture mirrors the financial instrument known as an option, as described [here](https://www.investopedia.com/terms/o/option.asp). Having worked in financial markets, I've seen firsthand how this mirrors the very instruments we trade. Just as a trader might buy call options to benefit from potential upside while limiting downside risk, we as architects can design systems that preserve our ability to capitalise on future opportunities while protecting against known risks.

I'm certainly not the only one to see this similarity — I read a similar comparison by Gregor Hohpe [here](https://architectelevator.com/architecture/architecture-options/). Simply put, an option is a financial instrument (contract) that is based on the value of an underlying asset.

While options can be used for various purposes — including income generation, trading, speculation, and hedging — the key use here is the ability to hedge or manage risk. This discussion does not explore the full range of financial options, but focuses specifically on architecture's ability to defer decisions while managing risk.

While having the flexibility to exercise or implement a specific option in the future is valuable for building a flexible architecture that manages risks, there is a cost associated with it (in the financial world, this is called the strike price).
Similarly, in architecture, the cost of maintaining optionality could include added development complexity, deferred decision-making overhead, or increased technical debt.

Sometimes, the simplest architectural approach initially might make future options more difficult or expensive to execute. However, this cost can often be considered part of the implied cost of the simplest option, especially when evaluating factors like time to market.

For example, in the case of startups, where time to market and testing various approaches are critical, the initial option may be to take a simple architectural approach with less focus on scalability, extensibility, or operational costs, in order to release quickly (I am not making any judgement here about whether this is a good or bad approach, but being scrappy and getting to market is definitely a thing). In this scenario, future options — such as scaling the system — may incur significant re-development costs. Yet, this is often a worthwhile price to pay if the product proves successful and the growth justifies additional investments, something which is not always known when attempting to start a new product. This is the moment when the option is exercised.

At other times, the options may be more complex, and careful consideration of the trade-offs is necessary.

This same thought came to mind when discussing options for architecture within government. In government contexts, political changes often require architectural flexibility to align with shifting strategic priorities — making architectural options even more valuable. This governmental parallel resonates strongly with my financial services experience. Just as political changes drive policy shifts, regulatory changes in financial markets create similar volatility. ASIC might introduce new market integrity rules, or global regulators might mandate new reporting requirements. Having worked through several such transitions, I've learned that the systems which survive and thrive are those architected with regulatory optionality from the start.

This provides an additional benefit but also consideration in the architectural strategy. As Gregor Hohpe makes the point about volatility ([Black Scholes model](https://en.wikipedia.org/wiki/Black%E2%80%93Scholes_model)) the value on an option increases in a time of high volatility (or change). Working in financial services has taught me this principle directly: in highly regulated industries like financial services, the value of architectural options increases with regulatory and market volatility. The more uncertain the environment, the more valuable it becomes to preserve flexibility.

## Real-World Financial Services Examples

**Market Data Architecture Options**
During my work in capital markets, I've observed how market data systems must be architected with optionality in mind. You might start with a simple market data feed that handles current trading volumes, but you need to preserve the option to:
- Scale to handle circuit-breaker scenarios (10x normal volume)
- Add new data types as markets evolve (crypto derivatives, ESG metrics)
- Integrate with international exchanges as cross-listings increase

The "strike price" here is the additional complexity in your messaging layer and data models, but the alternative—rebuilding your entire market data infrastructure during a market expansion—is far more expensive.

**Regulatory Compliance Options**
Financial services operate in one of the most regulated industries globally. When designing systems, we must consider:
- **MiFID III compliance**: Building transaction reporting that can adapt to rule changes without system overhauls
- **T+1 settlement**: Architecting settlement systems that could accelerate from T+2 to T+1 (and potentially to T+0) as regulations evolve
- **Open Banking**: Designing API layers that can support current needs while preserving the option for broader ecosystem integration

**Security Evolution Options**
In financial services, security isn't optional—but the specific implementation must remain flexible. Systems I've worked with needed to preserve options for:
- Upgrading from 2FA to hardware security keys as threat levels increased
- Implementing quantum-resistant encryption before it becomes mandatory
- Adding real-time fraud detection without disrupting core transaction flows

The cost of these options is ongoing architectural complexity, but the cost of not having them could be regulatory non-compliance or security breaches.

## A/B Testing

A practical example of maintaining options in digital architecture is A/B testing, where we deliberately design and implement multiple approaches to evaluate their effectiveness.

While more focused on user experience and product development, this is a related concept where we incur the option price of developing two different approaches and trial both, comparing both options to determine which is more effective.

Once architectural options have been identified, the next step is to evaluate these choices strategically. This includes assessing their feasibility, trade-offs, and alignment with the organisation's objectives.

---

## Evaluating Alternative Target Architectures and Trade-Offs
See also [Alternative Target Architecture and Trade-Offs]

### Criteria

* **Time and cost realising the alternative** — Evaluate the investment required relative to business value delivered.
* **Time period for estimated benefits** — Consider when tangible benefits will be realised following implementation.
* **Adherence to architecture guidelines** — Ensure compliance with architectural standards and principles.
* **Delivery (Buy, Build, Re-Use, Extend)** — Assess available delivery options based on strategic alignment and cost-effectiveness.
* **Impact on business capabilities** — Understand how the alternative will affect the organisation's ability to deliver services.
* **Risks associated with alternatives** — Identify potential risks, dependencies, and mitigations for each alternative.

## Lessons from Financial Markets

Working in financial services has taught me several key principles about architectural optionality:

**1. Volatility Increases Option Value**
Just as Gregor Hohpe noted about the Black-Scholes model, in highly regulated industries like financial services, the value of architectural options increases with regulatory and market volatility. The more uncertain the environment, the more valuable it becomes to preserve flexibility.

**2. Time Decay Matters**
Financial options lose value over time if not exercised. Similarly, architectural options that aren't maintained become harder to exercise. I've seen systems where the "option" to scale was theoretically preserved but became practically impossible due to accumulated technical debt.

**3. Risk-Free Rate Analogy**
In options pricing, the risk-free rate represents the baseline return. In architecture, this might be the "do nothing" option—the cost of maintaining status quo versus investing in optionality. Sometimes the safest architectural choice is actually the riskiest business choice.

**4. Exercise Discipline**
Not every option should be exercised. I've witnessed projects that maintained too many options for too long, creating unnecessary complexity. Like a trader, architects need discipline about when to exercise options and when to let them expire.

## Conclusion

The organisations that succeed are those that treat architectural decisions like portfolio management—carefully balancing risk and opportunity, maintaining options when uncertainty is high, and exercising them when conditions are right. 

The financial markets have taught us that the future is unpredictable, but with proper risk management and strategic optionality, we can build systems that not only survive uncertainty but profit from it. The same principles that make a good trader—discipline, risk awareness, and strategic thinking—make for robust architectural decisions.

In uncertain environments, architecture that preserves optionality isn't just a competitive advantage; in financial services, it's often the difference between compliance and violation, between capturing market opportunities and missing them entirely. By designing systems that allow stakeholders to defer decisions and adapt to change, architects create a foundation for resilience, innovation, and long-term business value.