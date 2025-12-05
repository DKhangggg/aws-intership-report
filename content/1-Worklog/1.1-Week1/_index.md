---
title: "Week 1 Worklog"
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Week 1 Objectives: Identity Management and Network Architecture (Sep 08 – Sep 12)

Establish an enterprise-grade AWS account and build a secure Virtual Private Cloud (VPC). This is the most critical phase, as misconfigurations during this stage often lead to security vulnerabilities and technical debt that are difficult to remediate later.

### Tasks Completed This Week:

| Day       | Main Activities                                                                                                                                                                                                                                                                                | Date       | Status    | Reference                                 |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------- | ----------------------------------------- |
| Monday    | **Account Initialization & Cost Management**<br>- Initialize AWS Account and secure Root User with MFA<br>- Set up AWS Budgets (Cost & Usage Budget)<br>- Configure Amazon SNS for budget alerts (80% threshold)<br>- Research AWS Support plans and SLA                                       | 09/08/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| Tuesday   | **IAM - Identity Management (Part 1)**<br>- Apply Least Privilege principle<br>- Create IAM User for administrators<br>- Create Groups: Admins, Developers, Auditors<br>- Assign Managed Policies (AdministratorAccess, PowerUserAccess)<br>- Set up Account Password Policy per CIS Benchmark | 09/09/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| Wednesday | **IAM - Identity Management (Part 2)**<br>- Create IAM Role for EC2 to access S3<br>- Understand Instance Metadata Service (IMDS)<br>- Write Custom Policy JSON (granular permissions)<br>- Practice limiting permissions by bucket and time                                                   | 09/10/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| Thursday  | **VPC - Theory & Design**<br>- Study Networking Essentials with Amazon VPC<br>- Differentiate Default VPC vs Custom VPC<br>- IP Planning: Design CIDR 10.0.0.0/16 (65,536 IPs)<br>- Design Multi-AZ: Public Subnets and Private Subnets                                                        | 09/11/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| Friday    | **VPC - Implementation & Security**<br>- Create Custom VPC, Subnets and Internet Gateway<br>- Configure Route Tables and NAT Gateway<br>- Configure Security Groups and NACL<br>- Apply Defense in Depth                                                                                       | 09/12/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |

### Week 1 Achievements:

**Security Infrastructure:**

- AWS account protected with MFA for Root User
- Clear IAM hierarchy (Users, Groups, Roles)
- Least Privilege principle applied to all policies
- Password Policy compliant with CIS Benchmark standards

**Network Architecture:**

- Complete Custom VPC with CIDR 10.0.0.0/16
- Multi-AZ design with Public and Private Subnets
- Properly configured Internet Gateway and NAT Gateway
- Route Tables clearly defining traffic flows

**Access Control:**

- Security Groups established in layered model
- Clear understanding of Security Groups (Stateful) vs NACL (Stateless)
- IAM Roles for EC2 instead of hard-coded credentials

**Financial Governance:**

- AWS Budgets with automatic alerts via SNS
- Strong understanding of FinOps model from the start
- Mastery of Support plans and SLAs

**Operational Skills:**

- Proficient with AWS Console for basic services
- Understanding of IMDS mechanism and temporary credentials
- Basic network troubleshooting
- Isolated, secure environment ready for application deployment

- Acquired the ability to connect between the web interface and CLI to manage AWS resources in parallel.
- ...
