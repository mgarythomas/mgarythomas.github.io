---
title: "Options: How an Architecture Manages Change and Uncertainty"
summary: "How an architecture provides options for stakeholders"
description: "How an architecture provides options for stakeholders"
draft: true
tags: ["options", "architecture"]
categories: ["architecture"]
author: "Gary Thomas"
date: 2025-04-26
---
How do we provide optionality for our stakeholders?

As anybody who has worked on technology projects for a while will know, some things are unknown at the beginning of a project or there may be additional requirements or changes of direction over time.

How Do We Provide Optionality for Our Stakeholders?

Anyone who has worked on technology projects will know that, at the beginning of a project, certain elements remain uncertain, or new requirements and changes of direction may arise over time.

This is why presenting options during the development of architecture and in engagement with various stakeholders is crucial. This concept isn’t unique to me; Gregor Hohpe and Michael Fowler have discussed the importance of offering options in architecture [here](https://martinfowler.com/articles/architect-elevator.html#SellArchitectureOptions).

In my perspective, the concept of providing options in architecture mirrors the financial instrument known as an option, as described [here](https://www.investopedia.com/terms/o/option.asp). Simply put, an option is a financial instrument (contract) that is based on the value of an underlying asset.

While options can be used for various purposes — including income generation, trading, speculation, and hedging — the key use here is the ability to hedge or manage risk. Our focus is not on the various types of options available but rather on the architecture’s ability to allow for future options without the need to commit to a specific choice today.

While having the flexibility to exercise or implement a specific option in the future is valuable for building a flexible architecture that manages risks, there is a cost associated with it (in the financial world, this is called the strike price).

Sometimes, the simplest approach initially might make future options more difficult or expensive to execute. However, this cost can often be considered part of the implied cost of the option, especially when evaluating factors like time to market.

For example, in the case of startups, where time to market and testing various approaches are critical, the initial option may be to take a simple approach without worrying about scalability, extensibility, or operational costs in order to release quickly. In this scenario, future options — such as scaling the system — may incur significant re-development costs. Yet, this is often a worthwhile price to pay if the product proves successful and the growth justifies additional investments. This is the moment when the option is exercised.

At other times, the options may be more complex, and careful consideration of the trade-offs is necessary.

---

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

### Gap Analysis

A Gap Analysis is a critical tool for identifying the differences between the current state of the architecture and the target state, which could include both functional and non-functional requirements. It helps identify what is missing or what needs to change to achieve the desired outcomes. The analysis should consider both immediate needs and future scalability, ensuring that strategic decisions are aligned with business objectives.

Here are some key areas to consider when performing a Gap Analysis:

- **Business Capabilities**
  - Current State: What business capabilities does the current architecture support?
  - Target State: What business capabilities are required to meet the future objectives?
  - Gap: Identify any areas where the current architecture is not enabling the business capabilities needed for growth.

- **Data Architecture & Management**
  - Current State: How is data currently managed within the architecture? What types of data are stored, and where is it stored (e.g., on-premise, in the cloud)?
  - Target State: What data needs to be collected, stored, and processed to meet future business goals?
  - Gap: Assess gaps in data management practices, including:
    - **Data Silos:** Are there areas where data is not easily shared or integrated across the enterprise?
    - **Data Quality:** Is the data accurate, consistent, and reliable?
    - **Scalability & Storage:** Can the current data architecture support future data growth?
    - **Data Access & Security:** Are sensitive data handling practices up to standard?
    - **Analytics & Insights:** Does the existing architecture support advanced analytics or AI/ML?
    - **Data Governance:** Is there a clear governance model to ensure data integrity and compliance?

- **Technology Stack & Infrastructure**
  - Current State: What technology stack and infrastructure are in place?
  - Target State: What changes are required to accommodate future demands?
  - Gap: Identify any gaps between the current technology stack and what will be required to meet future objectives.

- **Performance & Scalability**
  - Current State: What is the current performance level (speed, response times, availability, etc.)?
  - Target State: What performance levels are needed to support projected growth or usage?
  - Gap: Identify any performance bottlenecks or areas where the system may fail to scale effectively.

- **Security & Compliance**
  - Current State: What security measures and compliance standards are currently in place?
  - Target State: What additional security and compliance measures will be necessary as the system evolves?
  - Gap: Identify any areas where security practices may be outdated or incomplete.

- **Integration & Interoperability**
  - Current State: How well does the current system integrate with other systems, both internally and externally?
  - Target State: What future integrations will need to be implemented?
  - Gap: Identify systems or data sources that are difficult to integrate.

- **User Experience & Interface Design**
  - Current State: What user interfaces and experiences are currently in place?
  - Target State: What improvements are needed in terms of usability, accessibility, or mobile responsiveness?
  - Gap: Identify areas where the user interface or experience needs to be enhanced.

- **Documentation & Knowledge Management**
  - Current State: How well-documented are the existing systems, architecture, and processes?
  - Target State: What documentation will be required for future expansion?
  - Gap: Assess gaps in documentation and knowledge management, such as missing architectural diagrams or outdated manuals.

- **Resource Allocation & Skills**
  - Current State: Do we have the right skills and resources in place to support the current architecture?
  - Target State: Are new skills or resources needed?
  - Gap: Identify skill gaps and resource constraints that might affect the architecture’s scalability.

- **Cost & Time-to-Market**
  - Current State: What are the current project costs and timelines for delivering features?
  - Target State: What resources, timelines, and budgets are required for the target architecture?
  - Gap: Identify areas where cost overruns or delays may occur.

- **Vendor & Third-Party Dependencies**
  - Current State: What external vendors or third-party services are part of the current architecture?
  - Target State: Are new vendors or services needed to support the future vision?
  - Gap: Identify any gaps related to vendor capabilities, contract limitations, or dependence on third-party services.