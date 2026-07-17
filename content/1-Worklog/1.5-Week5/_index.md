---
title: "Week 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

**Weekly objectives:**
- Provision Amazon EC2 instances to run the web application in private subnets.
- Configure a Target Group and define robust HTTP health checks.
- Establish an Auto Scaling Group (ASG) with scaling policies to handle load spikes.
- Verify end-to-end network interconnection from load balancer to web server.

**Tasks to be deployed this week:**

| Day | Task | Date |
|---|---|---|
| Monday | Deployed compute instances on Amazon EC2 inside private subnets for web hosting. | May 18 |
| Tuesday | Created the `WebApp-TG` Target Group on port 3000 and configured health check endpoints. | May 19 |
| Wednesday | Linked the Target Group to the Application Load Balancer HTTP listeners on port 80. | May 20 |
| Thursday | Deployed the Auto Scaling Group `WebApp-ASG` with desired=2, min=1, max=4 capacities. | May 21 |
| Friday | Executed path routing tests and verified load balancing across active instances. | May 22 |

**Weekly results achieved:**
- **Monday:**
  - Result Achieved: Web servers provisioned successfully, reachable only through private network endpoints.
  - Lesson: Placing compute engines behind private subnets protects application code and databases from direct internet exploits.
- **Tuesday:**
  - Result Achieved: Target Group active. Defined health checks running every 30 seconds.
  - Lesson: Real-time health checks allow load balancers to automatically quarantine crashed servers without manual intervention.
- **Wednesday:**
  - Result Achieved: Integrated ALB and Target Group, verifying that incoming port 80 requests map to target port 3000.
  - Lesson: Mapping public web traffic to custom internal ports separates network concerns from application configurations.
- **Thursday:**
  - Result Achieved: Auto Scaling policies activated. Configured scale-up alerts based on average CPU usage exceeding 70%.
  - Lesson: ASG policies automate resource scaling, matching compute expenses to real-time traffic demand.
- **Friday:**
  - Result Achieved: Confirmed that traffic routed to the Load Balancer successfully reaches the backend web servers.
  - Lesson: Testing the complete integration path ensures that security group permissions do not block valid HTTP routes.
