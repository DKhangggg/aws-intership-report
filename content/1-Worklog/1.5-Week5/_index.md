---
title: "Week 5 Worklog"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives: Systems Management and Infrastructure as Code (Oct 06 – Oct 10)

Eliminate manual operations, manage large-scale server fleets, and encode infrastructure.

### Week 5 Objectives:

- Fast VPS: Deploy a complete WordPress application in 5 minutes using Amazon Lightsail.
- Containerization: Package a small application into a Docker Image and deploy on Lightsail Container Service.
- Elasticity: Set up self-healing and auto-scaling architecture with EC2 Auto Scaling Group.
- Load Balancing: Distribute user traffic through Application Load Balancer (ALB).

### Tasks to be carried out this week:

| Task ID    | Day | Work                                                                                                                                                                                | Start Date | Completion Date | Status    | Reference Material                        |
| ---------- | --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------- | ----------------------------------------- |
| T5.1       | 2   | **SSM - Fleet Management:** <br> - Configure EC2 IAM Role with AmazonSSMManagedInstanceCore policy <br> - Use Run Command to update packages across multiple instances              | 10/06/2025 | 10/06/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T5.2       | 3   | **Session Manager - Secure Access:** <br> - Close SSH port (22) on Security Group <br> - Access EC2 via Session Manager instead of traditional SSH                                  | 10/07/2025 | 10/07/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T5.3       | 4   | **CloudFormation - IaC Basics:** <br> - Write YAML template defining VPC and EC2 <br> - Create Stack and observe auto-provisioned resources                                         | 10/08/2025 | 10/08/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T5.4       | 4   | **CloudFormation - Stack Management:** <br> - Perform Update Stack with Change Sets <br> - Test Drift Detection feature to find manual changes                                      | 10/08/2025 | 10/09/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T5.5       | 5   | **AWS CDK - Initialize Project:** <br> - Install AWS CDK CLI <br> - Init TypeScript project: `cdk init app --language typescript`                                                   | 10/09/2025 | 10/09/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T5.6       | 5   | **AWS CDK - Define Infrastructure:** <br> - Use L2 Construct to create S3 Bucket <br> - Enable versioning and encryption in code                                                    | 10/09/2025 | 10/10/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T5.7       | 6   | **AWS CDK - Deploy & Test:** <br> - Run `cdk deploy` to deploy stack <br> - Observe CloudFormation ChangeSet and verify resources                                                   | 10/10/2025 | 10/10/2025      | Completed | <https://cloudjourney.awsstudygroup.com/> |
| **VoltGo** |     | **[PROJECT] VoltGo - React Native Setup**                                                                                                                                           |            |                 |           |                                           |
| VG5.1      | 2-6 | **Project Initialization:** <br> - Init Expo project with Expo Router <br> - Setup NativeWind (Tailwind for RN) <br> - Install dependencies: Lucide React Native, expo-secure-store | 10/06/2025 | 10/10/2025      | Completed | VoltGo Internal Docs                      |
| VG5.2      | 2-6 | **Folder Structure:** <br> - Create folder structure: app/(tabs), app/(auth), app/(rental), components/ <br> - Setup tsconfig with absolute imports (@/)                            | 10/06/2025 | 10/10/2025      | Completed | VoltGo Internal Docs                      |

### Week 5 achievements:

- **Comparison:**

  - Lightsail extremely fast to deploy but lacks deep network customization
  - Lightsail VPC Peering has limitations
  - Suitable for small projects, blogs, prototypes

- **Elastic System:**

  - Built a Fault Tolerant Web system
  - When manually terminating 1 instance, ASG immediately creates a new replacement instance
  - System automatically scales up/down based on demand

- **Load Balancing:**

  - ALB distributes requests evenly between instances
  - Ensures users don't experience service interruption when a server fails
  - Understanding of Health Checks and Drain Connection

- **Architecture:**
  - Solid grasp of Stateless Architecture concept
  - Cannot store uploaded files or sessions on EC2 hard drive
  - Combine S3 (files) and RDS (data) for Cloud-Native system
  - User Data for Bootstrapping is a key automation technique
