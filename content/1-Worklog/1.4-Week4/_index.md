---
title: "Week 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

**Weekly objectives:**
- Create and configure an Amazon CloudFront distribution to cache global static assets.
- Integrate AWS Web Application Firewall (WAF) to protect network endpoints.
- Provision an Internet-Facing Application Load Balancer (ALB) across multiple Availability Zones.
- Configure load balancing routing rules, listeners, and origin routing.

**Tasks to be deployed this week:**

| Day | Task | Date |
|---|---|---|
| Monday | Initialized the Amazon CloudFront configuration wizard and created the `WebApp-Distribution` pipeline. | May 11 |
| Tuesday | Configured the origin server definitions inside CloudFront to route traffic from the API Gateway endpoint. | May 12 |
| Wednesday | Optimized caching policies, configuring header forwarding rules and custom Time-To-Live (TTL) values. | May 13 |
| Thursday | Integrated AWS WAF with default rate-limiting security rules to protect the distribution against DDoS attacks. | May 14 |
| Friday | Provisioned the `WebApp-ALB` Application Load Balancer across two public Availability Zones (`ap-southeast-1a` & `1b`). | May 15 |

**Weekly results achieved:**
- **Monday:**
  - Result Achieved: Configured the baseline CloudFront distribution structure for edge caching.
  - Lesson: Using Content Delivery Networks (CDNs) dramatically decreases response latency for static content by placing it closer to users.
- **Tuesday:**
  - Result Achieved: Successfully routed CloudFront API requests through to the API Gateway origin endpoints.
  - Lesson: Origin configurations must use secure protocols (HTTPS) and match API endpoint host names to prevent routing failures.
- **Wednesday:**
  - Result Achieved: Tuned caching rules, enabling caching for images/CSS while bypassing cache for dynamic authentication APIs.
  - Lesson: Granular cache behaviors prevent user session data from being accidentally cached and exposed.
- **Thursday:**
  - Result Achieved: Active WAF protection layer. Tested basic IP rate limits to prevent brute-force attacks.
  - Lesson: Filtering malicious requests at the edge with WAF keeps backend compute engines safe and reduces resource usage.
- **Friday:**
  - Result Achieved: Load Balancer deployed and active. Verified internet-facing accessibility of the ALB DNS name.
  - Lesson: Running load balancers across multiple AZs ensures the system remains resilient if a single AZ experiences outages.
