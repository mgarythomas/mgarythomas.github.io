---
title: "Dev Team Capability & Maturity Assessment"
description: "A simple engineering assessment based on the DORA framework. This need not be completed in full."
draft: false
ShowToc: true
TocOpen: true
author: "Gary Thomas"
date: 2025-06-09
---

# Dev Team Capability & Maturity Assessment

## Instructions
This survey assesses your development team's capabilities across technical, process, and cultural dimensions based on the DORA (DevOps Research and Assessment) framework. Please answer honestly based on your current state, not aspirational goals.

**Rating Scale:**
- **1 - Not Implemented**: We don't do this at all
- **2 - Ad Hoc**: We do this inconsistently or only in some cases  
- **3 - Developing**: We do this regularly but it's not fully mature
- **4 - Mature**: We do this consistently with good practices
- **5 - Optimizing**: We do this excellently and continuously improve

---

## Section A: Technical Capabilities

### A1. Version Control & Code Management
**How effectively does your team manage code and changes?**  
📚 *References: [Git Best Practices](https://www.atlassian.com/git/tutorials/comparing-workflows) | [Conventional Commits](https://www.conventionalcommits.org/)*

1. **Version Control Usage** - All production code is stored in version control with meaningful commit messages
   - Rating: ___/5
   - Comments: _______________
   - 📖 *Learn more: [Git Workflow Best Practices](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)*

2. **Trunk-Based Development** - Teams work on shared branches with short-lived feature branches (< 1 day)
   - Rating: ___/5  
   - Comments: _______________
   - 📖 *Learn more: [Trunk-Based Development](https://trunkbaseddevelopment.com/) | [DORA on Trunk-Based Development](https://dora.dev/devops-capabilities/technical/trunk-based-development/)*

3. **Code Review Process** - All changes go through peer review before merging
   - Rating: ___/5
   - Comments: _______________
   - 📖 *Learn more: [Code Review Best Practices](https://google.github.io/eng-practices/review/) | [Pull Request Guidelines](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/getting-started/best-practices-for-pull-requests)*

### A2. Continuous Integration (CI)
**How well does your team integrate and validate code changes?**  
📚 *References: [Martin Fowler on CI](https://martinfowler.com/articles/continuousIntegration.html) | [DORA on CI](https://dora.dev/devops-capabilities/technical/continuous-integration/)*

4. **Automated Build Process** - Code changes trigger automated builds without manual intervention
   - Rating: ___/5
   - Comments: _______________
   - 📖 *Learn more: [CI/CD Pipeline Best Practices](https://www.gitlab.com/blog/2020/07/06/beginner-guide-ci-cd/) | [GitHub Actions Guide](https://docs.github.com/en/actions)*

5. **Build Speed** - Build and basic test suite completes in under 10 minutes
   - Rating: ___/5
   - Comments: _______________
   - 📖 *Learn more: [Optimizing Build Times](https://docs.gradle.org/current/userguide/performance.html) | [Fast CI/CD Practices](https://www.thoughtworks.com/insights/blog/architecting-continuous-delivery)*

6. **Build Reliability** - Builds fail only due to legitimate issues, not infrastructure problems
   - Rating: ___/5
   - Comments: _______________
   - 📖 *Learn more: [Reliable CI/CD Infrastructure](https://kubernetes.io/docs/concepts/overview/ci-cd/) | [Build Reliability Patterns](https://www.thoughtworks.com/insights/blog/architecting-continuous-delivery)*

### A3. Test Automation
**How comprehensive and effective is your automated testing?**  
📚 *References: [Test Pyramid](https://martinfowler.com/articles/practical-test-pyramid.html) | [DORA on Test Automation](https://dora.dev/devops-capabilities/technical/test-automation/)*

7. **Unit Test Coverage** - Adequate unit test coverage for critical business logic
   - Rating: ___/5
   - Comments: _______________
   - 📖 *Learn more: [Unit Testing Best Practices](https://martinfowler.com/bliki/UnitTest.html) | [Test Coverage Guidelines](https://testing.googleblog.com/2020/08/code-coverage-best-practices.html)*

8. **Integration Testing** - Automated tests verify component interactions
   - Rating: ___/5
   - Comments: _______________
   - 📖 *Learn more: [Integration Testing Strategies](https://martinfowler.com/articles/microservice-testing/) | [Contract Testing](https://pact.io/)*

9. **Test Data Management** - Reliable, maintainable test data and environments
   - Rating: ___/5
   - Comments: _______________
   - 📖 *Learn more: [Test Data Management](https://www.thoughtworks.com/insights/blog/test-data-management) | [Database Testing](https://www.liquibase.com/blog/database-testing-best-practices)*

### A4. Continuous Delivery (CD)
**How effectively can your team deploy software?**  
📚 *References: [Continuous Delivery Book](https://continuousdelivery.com/) | [DORA on Deployment Automation](https://dora.dev/devops-capabilities/technical/deployment-automation/)*

10. **Deployment Automation** - Deployments are largely automated with minimal manual steps
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Deployment Automation Patterns](https://martinfowler.com/articles/continuousDelivery.html) | [Infrastructure as Code](https://www.terraform.io/intro)*

11. **Environment Consistency** - Development, staging, and production environments are consistent
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Environment Parity](https://12factor.net/dev-prod-parity) | [Containerization Best Practices](https://docs.docker.com/develop/dev-best-practices/)*

12. **Deployment Frequency** - Team can deploy to production on-demand (daily or more frequently)
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Continuous Deployment](https://www.atlassian.com/continuous-delivery/continuous-deployment) | [Release Strategies](https://martinfowler.com/bliki/BlueGreenDeployment.html)*

### A5. Architecture & Design
**How well-designed and maintainable is your system architecture?**  
📚 *References: [Microservices Patterns](https://microservices.io/) | [DORA on Architecture](https://dora.dev/devops-capabilities/technical/architecture/)*

13. **Loosely Coupled Architecture** - Services/components can be developed and deployed independently
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Loosely Coupled Systems](https://martinfowler.com/articles/microservices.html) | [Team Topologies](https://teamtopologies.com/)*

14. **Code Maintainability** - Code is clean, well-documented, and easy to modify
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Clean Code Principles](https://www.oreilly.com/library/view/clean-code-a/9780136083238/) | [Documentation Best Practices](https://www.writethedocs.org/guide/writing/beginners-guide-to-docs/)*

15. **Technical Debt Management** - Team regularly addresses technical debt and refactoring
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Managing Technical Debt](https://martinfowler.com/bliki/TechnicalDebt.html) | [Refactoring Strategies](https://refactoring.com/)*

---

## Section B: Process & Measurement Capabilities

### B1. Lean Product Management
**How effectively does your team manage product development?**  
📚 *References: [Lean Startup](http://theleanstartup.com/) | [DORA on Lean Product Management](https://dora.dev/devops-capabilities/process/lean-product-management/)*

16. **Customer Feedback Integration** - Regular collection and incorporation of user feedback
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Customer Development](https://steveblank.com/category/customer-development/) | [User Research Methods](https://www.nngroup.com/articles/which-ux-research-methods/)*

17. **Work Visibility** - Clear visibility into work in progress and priorities
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Kanban Boards](https://www.atlassian.com/agile/kanban/boards) | [Work Visualization](https://kanbanize.com/kanban-resources/getting-started/what-is-kanban-board)*

18. **Small Batch Sizes** - Work is broken down into small, deliverable increments
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [User Story Slicing](https://www.agilealliance.org/glossary/story-splitting/) | [Feature Flags](https://martinfowler.com/articles/feature-toggles.html)*

### B2. Monitoring & Observability
**How well can your team understand system behavior and performance?**  
📚 *References: [Observability Engineering](https://www.oreilly.com/library/view/observability-engineering/9781492076438/) | [DORA on Monitoring](https://dora.dev/devops-capabilities/technical/monitoring-and-observability/)*

19. **Application Monitoring** - Comprehensive monitoring of application performance and health
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [APM Best Practices](https://www.datadoghq.com/knowledge-center/application-performance-monitoring/) | [SRE Monitoring](https://sre.google/sre-book/monitoring-distributed-systems/)*

20. **Log Management** - Centralized, searchable logging across systems
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Structured Logging](https://www.honeycomb.io/blog/structured-logging-and-your-team/) | [ELK Stack Guide](https://www.elastic.co/what-is/elk-stack)*

21. **Alerting & Incident Response** - Effective alerting that minimizes false positives
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Alerting Best Practices](https://docs.datadoghq.com/monitors/guide/alert-on-no-change-in-value/) | [Incident Response](https://response.pagerduty.com/)*

### B3. Performance Measurement
**How well does your team measure and track key metrics?**  
📚 *References: [Accelerate Book](https://itrevolution.com/accelerate-book/) | [DORA Research](https://dora.dev/research/)*

22. **DORA Metrics Tracking** - Team measures deployment frequency, lead time, MTTR, and change failure rate
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [DORA Metrics Guide](https://dora.dev/guides/dora-metrics-four-keys/) | [Measuring DevOps](https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance)*

23. **Business Metrics** - Development work is tied to measurable business outcomes
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [OKRs Guide](https://www.whatmatters.com/faqs/okr-meaning-definition-example/) | [Impact Mapping](https://www.impactmapping.org/)*

24. **Retrospectives & Improvement** - Regular retrospectives lead to concrete process improvements
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Retrospective Techniques](https://www.funretrospectives.com/) | [Continuous Improvement](https://www.atlassian.com/team-playbook/plays/retrospective)*

---

## Section C: Cultural Capabilities

### C1. Team Culture & Collaboration
**How effectively does your team work together?**  
📚 *References: [Psychological Safety](https://www.amazon.com/Fearless-Organization-Psychological-Workplace-Innovation/dp/1119477247) | [DORA on Culture](https://dora.dev/devops-capabilities/cultural/)*

25. **Psychological Safety** - Team members feel safe to speak up, ask questions, and admit mistakes
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Google's Project Aristotle](https://rework.withgoogle.com/blog/five-keys-to-a-successful-google-team/) | [Psychological Safety Guide](https://www.ccl.org/articles/leading-effectively-articles/what-is-psychological-safety-at-work/)*

26. **Cross-Functional Collaboration** - Development, QA, and operations work closely together
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [DevOps Collaboration](https://www.atlassian.com/devops/what-is-devops/devops-culture) | [Breaking Down Silos](https://itrevolution.com/articles/breaking-down-silos/)*

27. **Knowledge Sharing** - Team actively shares knowledge and avoids silos
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Knowledge Management](https://www.atlassian.com/team-playbook/plays/knowledge-sharing) | [Documentation Culture](https://www.writethedocs.org/guide/writing/beginners-guide-to-docs/)*

### C2. Learning & Innovation
**How well does your team learn and adapt?**  
📚 *References: [Learning Organization](https://www.amazon.com/Fifth-Discipline-Practice-Learning-Organization/dp/0385517254) | [DORA on Learning Culture](https://dora.dev/devops-capabilities/cultural/learning-culture/)*

28. **Continuous Learning** - Team members regularly learn new skills and technologies
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Learning Culture](https://hbr.org/2019/03/building-a-learning-culture) | [Tech Radar](https://www.thoughtworks.com/radar/how-to-byor)*

29. **Experimentation** - Team is encouraged to try new approaches and learn from failures
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Experimentation Culture](https://hbr.org/2020/03/building-a-culture-of-experimentation) | [Fail Fast Philosophy](https://www.lean-startup.co/fail-fast)*

30. **Time for Innovation** - Team has dedicated time for learning, experimentation, and improvement
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Google's 20% Time](https://www.google.com/about/careers/life-at-google/20-percent-time/) | [Innovation Time](https://www.atlassian.com/blog/teamwork/why-atlassian-gives-developers-20-percent-time-to-experiment)*

### C3. Organizational Support
**How well does the organization support effective software delivery?**  
📚 *References: [Accelerate Book](https://itrevolution.com/accelerate-book/) | [DORA on Transformational Leadership](https://dora.dev/devops-capabilities/cultural/transformational-leadership/)*

31. **Leadership Support** - Leadership actively supports DevOps practices and cultural change
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Transformational Leadership](https://dora.dev/devops-capabilities/cultural/transformational-leadership/) | [DevOps Leadership](https://itrevolution.com/articles/devops-leadership/)*

32. **Resource Allocation** - Team has adequate resources (time, tools, training) to do their job well
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Resource Planning](https://www.atlassian.com/agile/project-management/capacity-planning) | [Tool Investment ROI](https://www.mckinsey.com/capabilities/mckinsey-digital/our-insights/developer-velocity-how-software-excellence-fuels-business-performance)*

33. **Change Management** - Organization handles change effectively with clear communication
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Change Management](https://www.kotter.com/methodology/8-steps/) | [DevOps Transformation](https://dora.dev/guides/devops-culture-transform/)*

---

## Section D: Current State Assessment

### Team Information
- **Team Name**: _______________
- **Team Size**: _______________
- **Primary Technology Stack**: _______________
- **Average Tenure on Team**: _______________

---

## Section K: Service Portfolio & Architecture

### Current Service Landscape
**Describe your team's current service portfolio and codebase structure**

**Repository Management:**
- **Total number of repositories your team owns/maintains**: _______________
- **Active repositories (updated in last 6 months)**: _______________
- **Legacy/dormant repositories**: _______________
- **Monorepo vs Multi-repo approach**: _______________

**Deployable Artifacts:**
- **Total number of deployable services/applications**: _______________
- **Microservices count**: _______________
- **Monolithic applications count**: _______________
- **Batch jobs/scheduled processes**: _______________
- **Shared libraries/packages**: _______________
- **Database schemas managed**: _______________

**Service Types:** (Check all that apply)
- [ ] Web applications (frontend)
- [ ] REST APIs/Web services
- [ ] GraphQL APIs
- [ ] Message/event processors
- [ ] Background workers/job processors
- [ ] Data pipelines/ETL processes
- [ ] Machine learning models/services
- [ ] Static sites/documentation
- [ ] Mobile app backends
- [ ] Integration/middleware services
- [ ] Other: _______________

**Technology Diversity:**
- **Programming languages in use**: _______________
- **Database technologies**: _______________
- **Messaging/queue systems**: _______________
- **External service dependencies**: _______________

---

## Section L: Deployment Process Deep Dive

### Current Deployment Reality
**Walk us through exactly how deployments work today**

**Deployment Frequency by Environment:**
- **Development/Feature environments**: _______________ (times per day/week)
- **Staging/Testing environments**: _______________ (times per day/week)  
- **Production environments**: _______________ (times per day/week)

**Deployment Process Steps:**
*Please describe the actual steps a developer follows to deploy something new or modified to production:*

**Step 1:** _______________

**Step 2:** _______________

**Step 3:** _______________

**Step 4:** _______________

**Step 5:** _______________

*Continue numbering as needed...*

**Deployment Characteristics:**
- **Typical deployment duration**: _______________
- **Rollback time if needed**: _______________
- **Number of people required for production deployment**: _______________
- **Time of day restrictions for deployments**: _______________
- **Deployment approval requirements**: _______________

**Deployment Automation Level:**
- **Fully automated (zero-touch)**: ____ % of deployments
- **Semi-automated (some manual steps)**: ____ % of deployments  
- **Mostly manual**: ____ % of deployments
- **Completely manual**: ____ % of deployments

**Environment Promotion:**
How do changes move through environments?
- [ ] Automatic promotion after successful tests
- [ ] Manual promotion with approval gates
- [ ] Scheduled batch promotions
- [ ] Ad-hoc promotion as needed
- [ ] Other: _______________

**Deployment Challenges:**
What are the biggest pain points in your current deployment process?

1. _______________
2. _______________
3. _______________

**Database Changes:**
How are database schema changes handled?
- **Process**: _______________
- **Tools used**: _______________
- **Coordination required**: _______________

**Configuration Management:**
How are configuration changes deployed?
- **Process**: _______________
- **Environment-specific configs**: _______________
- **Secret/credential updates**: _______________

**Monitoring Deployment Success:**
How do you know a deployment was successful?
- **Automated health checks**: _______________  
- **Manual verification steps**: _______________
- **Rollback triggers**: _______________

---

## Section M: Service Dependencies & Integration

### Dependency Mapping
**Understanding your service ecosystem**

**Internal Dependencies:**
- **Services your team depends on (from other teams)**: _______________
- **Services that depend on yours**: _______________
- **Shared databases/resources**: _______________

**External Dependencies:**
- **Third-party APIs/services**: _______________
- **Cloud service dependencies**: _______________
- **On-premise system integrations**: _______________

**Dependency Management:**
- **How do you handle breaking changes from dependencies?**: _______________
- **Service contract/API versioning strategy**: _______________
- **Dependency update frequency**: _______________

**Data Flow:**
- **Primary data sources**: _______________
- **Data destinations/consumers**: _______________
- **Real-time vs batch processing**: _______________

---

## Section N: Operational Complexity

### Day-to-Day Operations
**Understanding the operational overhead**

**Support & Maintenance:**
- **On-call rotation requirements**: _______________
- **Average incidents per month**: _______________
- **Most common incident types**: _______________

**Environment Management:**
- **Number of environments maintained**: _______________
- **Environment provisioning time**: _______________
- **Environment cost (if known)**: _______________

**Release Coordination:**
- **Cross-team coordination required**: _______________
- **Release planning lead time**: _______________
- **Communication overhead**: _______________

**Technical Debt Impact:**
- **Time spent on maintenance vs new features**: ____% maintenance / ____% new features
- **Legacy system maintenance burden**: _______________
- **Modernization/refactoring priorities**: _______________

### Current Performance Metrics
Please provide approximate values if known:

- **Deployment Frequency**: _______________
- **Lead Time for Changes**: _______________  
- **Mean Time to Recovery (MTTR)**: _______________
- **Change Failure Rate**: _______________%

### Biggest Challenges
What are the top 3 challenges your team faces in software delivery?

1. _______________
2. _______________
3. _______________

### Improvement Priorities
What are the top 3 areas your team most wants to improve?

1. _______________
2. _______________
3. _______________

---

## Section E: Security & Compliance Capabilities

### E1. Security Integration
**How well is security integrated into your development process?**  
📚 *References: [DevSecOps](https://www.devsecops.org/) | [OWASP DevSecOps Guideline](https://owasp.org/www-project-devsecops-guideline/)*

34. **Security by Design** - Security considerations are integrated from the beginning of development
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Secure by Design](https://owasp.org/www-project-secure-by-design/) | [Threat Modeling](https://owasp.org/www-community/Threat_Modeling)*

35. **Automated Security Testing** - Security testing is automated and integrated into CI/CD pipeline
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [SAST/DAST Tools](https://owasp.org/www-community/Source_Code_Analysis_Tools) | [Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)*

36. **Vulnerability Management** - Regular scanning and timely remediation of security vulnerabilities
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Vulnerability Management](https://owasp.org/www-project-vulnerability-management-guide/) | [CVE Process](https://www.cve.org/)*

37. **Secrets Management** - Proper handling and storage of API keys, passwords, and certificates
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Secrets Management](https://www.hashicorp.com/resources/what-is-secrets-management) | [Best Practices](https://docs.github.com/en/actions/security-guides/encrypted-secrets)*

### E2. Compliance & Governance
**How well does your team manage compliance and governance requirements?**  
📚 *References: [IT Compliance](https://www.isaca.org/) | [Privacy by Design](https://www.ipc.on.ca/wp-content/uploads/resources/7foundationalprinciples.pdf)*

38. **Regulatory Compliance** - Team understands and implements required compliance standards (GDPR, SOX, etc.)
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [GDPR Compliance](https://gdpr.eu/compliance/) | [SOX Compliance](https://www.sox-online.com/)*

39. **Audit Trail** - Changes and deployments are properly logged and auditable
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Audit Logging](https://www.sans.org/white-papers/1168/) | [Compliance Automation](https://www.chef.io/solutions/compliance-automation)*

40. **Data Privacy** - Personal and sensitive data is properly protected and handled
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Data Protection](https://www.gdpr.org/data-protection/) | [Privacy Engineering](https://www.nist.gov/privacy-framework)*

---

## Section F: Sustainability & Efficiency

### F1. Environmental Sustainability
**How environmentally conscious is your software development?**  
📚 *References: [Green Software Foundation](https://greensoftware.foundation/) | [Sustainable Software Engineering](https://docs.microsoft.com/en-us/learn/modules/sustainable-software-engineering-overview/)*

41. **Resource Efficiency** - Code and infrastructure are optimized for energy efficiency
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Green Software Patterns](https://patterns.greensoftware.foundation/) | [Carbon Efficient Computing](https://www.microsoft.com/en-us/research/project/carbon-efficient-computing/)*

42. **Sustainable Architecture** - System design considers environmental impact and resource usage
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Sustainable Software Architecture](https://www.thoughtworks.com/insights/blog/sustainable-software-architecture) | [Green Computing](https://www.epa.gov/greeningepa/green-computing)*

43. **Green Computing Practices** - Team considers carbon footprint in technology decisions
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Carbon Aware Computing](https://github.com/Green-Software-Foundation/carbon-aware-sdk) | [Sustainability Metrics](https://www.accenture.com/us-en/insights/technology/green-software)*

### F2. Developer Experience & Productivity
**How optimized is the developer experience?**  
📚 *References: [Developer Experience](https://dx.devex.com/) | [SPACE Framework](https://queue.acm.org/detail.cfm?id=3454124)*

44. **Developer Tooling** - Developers have efficient, modern tools that support productivity
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Developer Tools Survey](https://insights.stackoverflow.com/survey/) | [IDE Best Practices](https://www.jetbrains.com/help/idea/getting-started.html)*

45. **Local Development Environment** - Easy setup and maintenance of local development environments
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Development Environment Setup](https://www.docker.com/blog/containerized-development-environments/) | [Codespaces](https://github.com/features/codespaces)*

46. **Documentation Quality** - Code, APIs, and processes are well-documented and accessible
    - Rating: ___/5
    - Comments: _______________
    - 📖 *Learn more: [Documentation Best Practices](https://www.writethedocs.org/guide/) | [API Documentation](https://swagger.io/specification/)*documented and accessible
    - Rating: ___/5
    - Comments: _______________

---

## Section G: Platform Engineering & Infrastructure

### G1. Platform Capabilities
**How mature is your platform and infrastructure management?**

47. **Infrastructure as Code** - Infrastructure is defined, versioned, and managed as code
    - Rating: ___/5
    - Comments: _______________

48. **Container/Cloud Native** - Applications are designed for modern deployment platforms
    - Rating: ___/5
    - Comments: _______________

49. **Self-Service Capabilities** - Developers can provision resources and environments independently
    - Rating: ___/5
    - Comments: _______________

50. **Platform Reliability** - Internal platforms and shared services have high availability
    - Rating: ___/5
    - Comments: _______________

### G2. Data & Analytics
**How well does your team manage and leverage data?**

51. **Data Quality** - Data used by applications is accurate, consistent, and reliable
    - Rating: ___/5
    - Comments: _______________

52. **Analytics Integration** - Applications properly instrument and expose business metrics
    - Rating: ___/5
    - Comments: _______________

53. **Data Governance** - Clear policies and processes for data access and usage
    - Rating: ___/5
    - Comments: _______________

---

## Section H: Advanced Team Dynamics

### H1. Cognitive Load Management
**How well does your team manage complexity and cognitive load?**

54. **Complexity Management** - Team actively works to reduce unnecessary complexity
    - Rating: ___/5
    - Comments: _______________

55. **Context Switching** - Developers can focus on tasks without excessive interruptions
    - Rating: ___/5
    - Comments: _______________

56. **Team Topology** - Team structure and responsibilities are clear and well-defined
    - Rating: ___/5
    - Comments: _______________

### H2. External Collaboration
**How effectively does your team collaborate externally?**

57. **Cross-Team Dependencies** - Dependencies on other teams are well-managed and minimized
    - Rating: ___/5
    - Comments: _______________

58. **Stakeholder Communication** - Regular, effective communication with business stakeholders
    - Rating: ___/5
    - Comments: _______________

59. **Vendor/Third-Party Management** - Effective management of external dependencies and services
    - Rating: ___/5
    - Comments: _______________

---

## Section I: Emerging Technology & Innovation

### I1. AI/ML Integration
**How well is your team positioned for AI/ML integration?**

60. **AI/ML Readiness** - Team understands and can implement AI/ML solutions where appropriate
    - Rating: ___/5
    - Comments: _______________

61. **Data for AI** - Data infrastructure supports AI/ML workloads and experimentation
    - Rating: ___/5
    - Comments: _______________

62. **AI Ethics & Governance** - Team considers ethical implications of AI implementations
    - Rating: ___/5
    - Comments: _______________

### I2. Future-Proofing
**How prepared is your team for future technological changes?**

63. **Technology Radar** - Team actively monitors and evaluates emerging technologies
    - Rating: ___/5
    - Comments: _______________

64. **Adaptability** - Team can quickly adapt to new technologies and changing requirements
    - Rating: ___/5
    - Comments: _______________

65. **Innovation Time** - Team has dedicated time for exploring new technologies and approaches
    - Rating: ___/5
    - Comments: _______________

---

## Section J: Additional Context

### Tools & Technology
List the primary tools your team uses:

- **Version Control**: _______________
- **CI/CD Platform**: _______________
- **Testing Frameworks**: _______________
- **Monitoring/Observability**: _______________
- **Project Management**: _______________
- **Communication**: _______________

### Organizational Context
- **Industry/Domain**: _______________
- **Regulatory Requirements**: _______________
- **Team Model** (Product team, feature team, etc.): _______________
- **Reporting Structure**: _______________

---

## Scoring Guide

### Capability Maturity Levels

**Score Range | Maturity Level | Description**
- **33-66**: **Foundational** - Basic practices in place, significant room for improvement
- **67-99**: **Developing** - Good practices emerging, some areas still need work  
- **100-132**: **Mature** - Solid practices across most areas, continuous improvement happening
- **133-165**: **Advanced** - Excellent practices, serving as model for others

### Next Steps
Based on your scores, consider:

1. **Focus Areas**: Lowest-scoring sections indicate priority improvement areas
2. **Quick Wins**: Look for capabilities rated 2-3 that could quickly move to 4
3. **Strategic Investments**: Consider longer-term improvements for foundational capabilities
4. **Cultural Barriers**: Address organizational and cultural impediments to technical improvements

---

*This survey is based on the DORA (DevOps Research and Assessment) capabilities framework and research. For more information, visit [dora.dev](https://dora.dev)*