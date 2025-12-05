---
title: "Week 10 Worklog"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives: Kubernetes on AWS - EKS (Nov 10 – Nov 14)

Manage large-scale microservices applications with EKS and Kubernetes.

### Week 10 Objectives:

- Build API: Create RESTful API for a Book Store management application.
- Serverless Logic: Write Lambda functions to perform CRUD (Create, Read, Update, Delete).
- NoSQL Storage: Design high-performance DynamoDB table.
- Integration: Connect API Gateway -> Lambda -> DynamoDB.

### Tasks to be carried out this week:

| Task ID    | Day | Work                                                                                                                                                                                       | Start Date | Completion Date | Status    | Reference Material                        |
| ---------- | --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | --------- | ----------------------------------------- |
| T10.1      | 2   | **Lambda - Basic Function:** <br> - Write Lambda function in Python for business logic <br> - Configure environment variables and timeout                                                  | 11/10/2025 | 11/10/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T10.2      | 2   | **DynamoDB - NoSQL Table:** <br> - Create DynamoDB table with Partition + Sort Key <br> - Enable Streams for event-driven processing                                                       | 11/10/2025 | 11/11/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T10.3      | 3   | **Lambda - DynamoDB Integration:** <br> - Write Lambda CRUD operations with boto3 <br> - Test with sample data and verify results                                                          | 11/11/2025 | 11/12/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T10.4      | 4   | **API Gateway - REST API:** <br> - Create REST API with multiple resources <br> - Configure Lambda proxy integration                                                                       | 11/12/2025 | 11/13/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T10.5      | 5   | **Cognito - Authentication:** <br> - Create Cognito User Pool as authorizer <br> - Protect API endpoints with JWT tokens                                                                   | 11/13/2025 | 11/14/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T10.6      | 6   | **Step Functions - Workflow:** <br> - Design state machine for complex workflow <br> - Orchestrate multiple Lambda functions                                                               | 11/14/2025 | 11/14/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| **VoltGo** |     | **[PROJECT] VoltGo - Admin Dashboard (Support Role)**                                                                                                                                      |            |                 |           |                                           |
| VG10.1     | 2-3 | **Web Setup - Next.js:** <br> - Init Next.js 14 project with App Router <br> - Setup Tailwind CSS and shadcn/ui components <br> - Project structure: app/(admin), app/(staff), components/ | 11/10/2025 | 11/11/2025      | Completed | VoltGo Web Docs                           |
| VG10.2     | 4-5 | **Admin Layout:** <br> - Sidebar navigation for admin routes <br> - Header with role-based menu <br> - Protected routes middleware                                                         | 11/12/2025 | 11/13/2025      | Completed | VoltGo Figma Design                       |
| VG10.3     | 6   | **Admin Dashboard:** <br> - Overview stats (Revenue, Users, Trips, Stations) <br> - Charts: Revenue trends, Trip analytics <br> - System health monitoring                                 | 11/14/2025 | 11/14/2025      | Completed | VoltGo Web Docs                           |

### Week 10 achievements:

- **Product:**

  - A complete operational backend API
  - No servers needed (No EC2)
  - Truly serverless architecture

- **Performance:**

  - Extremely fast response time (< 100ms)
  - Can handle thousands of requests/second by default
  - Auto scaling without configuration

- **Cost:**

  - Nearly $0 during development phase
  - Thanks to Lambda and DynamoDB Free Tier
  - Pay-per-request model

- **Architecture:**
  - Understanding of Microservices architecture
  - Event-driven programming
  - API-first design
  - NoSQL data modeling
