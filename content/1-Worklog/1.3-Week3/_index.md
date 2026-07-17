---
title: "Week 3"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

**Weekly objectives:**
- Study the requirements of the Fashion Retail Web App & ML Pipeline project.
- Understand the system architecture and the Decoupled architecture pattern.
- Design the network subnet mapping and security group boundaries.
- Define the database schemas and the data flow route for time-series forecasting.

**Tasks to be deployed this week:**

| Day | Task | Date |
|---|---|---|
| Monday | Analyzed the project business requirements for fashion inventory optimization and sales demand forecasting. | May 04 |
| Tuesday | Explored the Decoupled System Architecture Diagram, separating the Web Application & APIs from the ML Pipeline. | May 05 |
| Wednesday | Mapped out the network topology, including public/private subnets, CloudFront, ALB, and secure database subnets. | May 06 |
| Thursday | Designed the relational schemas for transactional records (`fashiondb`) and processed training features (`trainingdb`). | May 07 |
| Friday | Initialized the repository structure and planned the 10-phase workshop deployment roadmap. | May 08 |

**Weekly results achieved:**
- **Monday:**
  - Result Achieved: Documented the business rules, determining that time-series models will forecast demand to optimize stock.
  - Lesson: Understanding business constraints beforehand prevents design flaws during technical implementation.
- **Tuesday:**
  - Result Achieved: Approved the overall system architecture, choosing to separate user interfaces from heavy data processing services.
  - Lesson: Decoupling architectures ensures that a heavy training workload does not impact the frontend retail website's performance.
- **Wednesday:**
  - Result Achieved: Created security group routing rules, ensuring web servers can only accept traffic from the Load Balancer.
  - Lesson: Isolating backend instances in private subnets with restricted ingress rules minimizes the attack surface.
- **Thursday:**
  - Result Achieved: Finalized database schemas, detailing fields for stores, products, transactions, and rolling lag features.
  - Lesson: Decoupling live business tables from analytical training tables prevents performance degradation on transactional databases.
- **Friday:**
  - Result Achieved: Setup the directory structure following modular monolith patterns.
  - Lesson: Clear boundary definitions at the start of a project avoid deep circular dependencies later.
