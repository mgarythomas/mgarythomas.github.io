---
title: "Options"
summary: "How do we provide optionality for our stakeholders?"
draft: true
tags: ["options", "architecture"]
categories: ["architecture"]
author: "Gary Thomas"
date: 2025-04-26
---
How do we provide optionality for our stakeholders?

As anybody who has worked on technology projects for a while will know, some things are unknown at the beginning of a project or there may be additional requirements or changes of direction over time.

This is why the presenting of options is important when developing the architecture and engaging with different stakeholders. This is not my unique thought, there has been previous discussion of [options](https://martinfowler.com/articles/architect-elevator.html#SellArchitectureOptions) by Gregor Hohpe and Michael Fowler.

The way I would describe this is based very clearly on the way in which the financial instrument works [options](https://www.investopedia.com/terms/o/option.asp). Simply put, an option is a financial instrument (contract) that is based on the value of an underlying asset.

While options have many features and can be used for different purposes (income, trading and speculation, hedging), the use we are focussing on is the ability to hedge or *manage risk*. I don't want to go into to detail about the different types of options, but we are focussing on the ability of an architecture to allow future options without having to commit to the specific option today.

While being able to exercise or implement a specific option in the future sounds like good practice for a flexible architecture to manage risks, it will have some associated cost (in the financial instrument this is the strike price). Sometimes the simplest approach to begin with may make future options quite difficult or costly but often this can be considered part of the implied cost of the option when considering such factors as time to market.

Think of the a simplistic scenario with startups, where time to market and testing different approaches is critical. The option may be to take simple approaches and not worry about scaling, extensibility or operational costs in order to release early. This means that the option in the future may incur significant re-development (the cost), but this price is worth paying if the product is proving to be successful and the growth of the product warrants the additional costs. This is the point at which the option is exercised.

At other times, the options may be more complex, and the trade-offs have to be considered.

## Alternative Target Architecture and Trade-Offs
See also [Alternative Target Architecture and Trade-Offs]

### Criteria

* Time and cost realising the alternative
* Time period for estimated benefits
* Adherence to architecture guidelines
* Delivery - (Buy, Build, Re-Use, Extend)
* Impact on business capabilities
* Risks associated with alternatives

### Gap Analysis