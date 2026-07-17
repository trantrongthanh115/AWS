---
title: "Week 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

**Weekly objectives:**
- SSH into the production EC2 Web Server instance and set up environment dependencies.
- Install Git, Node.js (via NVM), and the PM2 process manager on the cloud node.
- Configure production environment variables (`DATABASE_URL`, `API_URL`, `PORT`).
- Deploy the Web Application backend and frontend, using PM2 to manage processes.
- Configure Nginx as a reverse proxy to route port 80 traffic to the internal Node.js port.

**Tasks to be deployed this week:**

| Day | Task | Date |
|---|---|---|
| Monday | Connected to the production EC2 instance via SSH and ran operating system package updates. | Jun 29 |
| Tuesday | Installed Git, Node.js (using NVM), and the PM2 runtime process manager on the instance. | Jun 30 |
| Wednesday | Cloned the web application codebase and configured production environmental settings (`.env`). | Jul 01 |
| Thursday | Configured and launched the backend web server on internal port 3000 using PM2. | Jul 02 |
| Friday | Installed Nginx, configured reverse proxy routing policies, and verified site access via the ALB DNS name. | Jul 03 |

**Weekly results achieved:**
- **Monday:**
  - Result Achieved: Verified secure SSH access and updated server security patches.
  - Lesson: Limiting SSH ingress permissions in the Security Group to specific admin IP addresses protects compute nodes from brute-force attempts.
- **Tuesday:**
  - Result Achieved: Deployed Node.js runtime and PM2 tools.
  - Lesson: Node Version Manager (NVM) allows developers to match local development runtime versions in production environments.
- **Wednesday:**
  - Result Achieved: Established connections to database endpoints and loaded database variables.
  - Lesson: Enforcing the separation of code and configuration settings using environment files is crucial for cloud deployments.
- **Thursday:**
  - Result Achieved: Verified that backend API services run persistently under PM2 supervision.
  - Lesson: PM2 handles automatic crash recovery and process monitoring, ensuring high availability.
- **Friday:**
  - Result Achieved: Nginx reverse proxy active. The web portal was successfully resolved through the Load Balancer DNS name.
  - Lesson: Setting up a reverse proxy like Nginx isolates application servers from direct client traffic, improving scalability.
