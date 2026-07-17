---
title: "Week 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

**Weekly objectives:**
- Design the user interface layout for the Global Fashion Retail web portal.
- Implement JWT-based secure authentication with an 8-hour session expiration rule.
- Integrate Multi-Factor Authentication (2FA TOTP) using Google Authenticator QR codes.
- Implement Role-Based Access Control (RBAC) mapping Admin, Manager, and Associate views.
- Integrate interactive charts displaying actual sales compared to machine learning forecast metrics.

**Tasks to be deployed this week:**

| Day | Task | Date |
|---|---|---|
| Monday | Designed the frontend layout for the Global Fashion Retail web portal dashboard using React. | Jun 22 |
| Tuesday | Programmed backend authentication middleware to issue and verify signed JWT user session tokens. | Jun 23 |
| Wednesday | Coded the 2FA enrollment wizard, rendering QR codes for Google Authenticator pairing. | Jun 24 |
| Thursday | Implemented RBAC access routing logic, separating Admin controls from standard Manager views. | Jun 25 |
| Friday | Integrated interactive visualization components mapping actual transactions alongside forecasting charts. | Jun 26 |

**Weekly results achieved:**
- **Monday:**
  - Result Achieved: Built responsive CSS dashboard layouts featuring bento grids and navigation menus.
  - Lesson: User interfaces should be clear and intuitive to help business administrators quickly interpret inventory warnings.
- **Tuesday:**
  - Result Achieved: Secured API backend routes, rejecting calls containing missing or expired JWT tokens.
  - Lesson: JWT sessions eliminate database lookup calls for session validation on every HTTP request.
- **Wednesday:**
  - Result Achieved: Successfully paired authenticators and enforced verification during login routines.
  - Lesson: 2FA secures user accounts, protecting corporate portals from credential compromise.
- **Thursday:**
  - Result Achieved: Verified that role-based permissions restrict UI panels and database update queries.
  - Lesson: RBAC prevents ordinary employees from accessing administrative database functions or triggering expensive model retraining.
- **Friday:**
  - Result Achieved: Rendered interactive line charts plotting real-time actual sales and predictive boundaries.
  - Lesson: Visualizing sales data alongside forecast lines helps managers make better inventory stocking decisions.
