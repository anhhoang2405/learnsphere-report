---
title: "Week 4 Worklog"
date: 2026-07-25
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

# 4. Core Backend APIs & JWT Auth Middleware

### Week Objectives:

* Design and implement backend APIs for course management, lesson assets, and quizzes.
* Set up secure token-based JWT authentication and role-based route authorization (Tutor/Student/Admin).

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date |
| --- | --- | --- | --- |
| 1 | Installed and configured `jsonwebtoken` and `bcryptjs` libraries to encrypt passwords and handle secure sessions. | 06/07/2026 | 06/07/2026 |
| 2 | Codeveloped user auth endpoints (Registration & Login), storing hashed credentials in MongoDB Atlas. | 07/07/2026 | 07/07/2026 |
| 3 | Developed a token-validation middleware (`authMiddleware`) to protect private application endpoints. | 08/07/2026 | 08/07/2026 |
| 4 | Implemented access-control middlewares (`roleMiddleware`) to validate user scopes (Student vs. Tutor vs. Admin). | 09/07/2026 | 09/07/2026 |
| 5 | Co-developed course CRUD routes (allowing draft/published switching) and lesson association controllers with Dung. | 10/07/2026 | 10/07/2026 |

### Week Achievements:

* Successfully established a secure JWT authentication and Role-Based Access Control (RBAC) foundation.
* Completed core CRUD API sets for courses, lessons, and quiz schema operations.aries for clean list layouts and media streaming.
