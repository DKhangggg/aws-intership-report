---
title: "Week 3 Worklog"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives: Databases and Managed Services (Sep 22 – Sep 26)

Transition from self-managed databases on EC2 to using Managed Database services (RDS, DynamoDB) to reduce operational overhead.

### Tasks Completed This Week:

- Compute Deployment: Successfully launch an EC2 Instance in the Public Subnet of the created VPC.
- Access Management: Configure Key Pair (ED25519) and Security Group for secure SSH access.
- Application Authorization: Use IAM Role to grant S3 access to EC2 without storing Access Keys on the machine.
- Block Storage: Create, attach, and format an additional EBS Volume to understand persistent storage.

### Tasks to be carried out this week:

| Day       | Main Activities                                                                                                                                                                      | Date                                                                                                                                                                    | Status     | Reference                                 |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ----------------------------------------- | --------- | ----------------------------------------- |
| Monday    | **Amazon RDS - Relational Database**<br>- Deploy RDS with MySQL/PostgreSQL<br>- Enable Multi-AZ Deployment<br>- Understand Synchronous Replication and Automatic Failover            | 09/22/2025                                                                                                                                                              | Completed  | <https://cloudjourney.awsstudygroup.com/> |
| Tuesday   | **RDS - Connection and Operations**<br>- Configure Security Group (only from Web-SG)<br>- Customize Parameter Groups<br>- Automated Backups and Manual Snapshot<br>- Perform Restore | 09/23/2025                                                                                                                                                              | Completed  | <https://cloudjourney.awsstudygroup.com/> |
| Wednesday | **DynamoDB - NoSQL Database**<br>- Create Users table with Partition Key<br>- Practice PutItem, GetItem, Query, Scan<br>- Compare Provisioned vs On-Demand                           | 09/24/2025                                                                                                                                                              | Completed  | <https://cloudjourney.awsstudygroup.com/> |
| Thursday  | **ElastiCache and HA Architecture**<br>- Deploy Redis cluster<br>- Apply Lazy Loading pattern<br>- Build 3-tier architecture with ALB                                                | 09/25/2025                                                                                                                                                              | Completed  | <https://cloudjourney.awsstudygroup.com/> |
| Friday    | **Directory Services**<br>- Learn AWS Managed Microsoft AD<br>- Integrate Windows EC2 into domain<br>- Centralized management via GPO                                                | 09/26/2025                                                                                                                                                              | Completed  | <https://cloudjourney.awsstudygroup.com/> |
| ---       | ---                                                                                                                                                                                  | ---                                                                                                                                                                     | ---        | ---                                       | ---       | ---                                       |
| T3.1      | 2                                                                                                                                                                                    | **EC2 - AMI Selection:** <br> - Select Amazon Linux 2023 AMI (HVM) <br> - Optimize default performance and security                                                     | 09/22/2025 | 09/22/2025                                | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T3.2      | 2                                                                                                                                                                                    | **Security - Key Management:** <br> - Create ED25519 Key Pair (more secure than RSA) <br> - Store .pem file locally with permission 400                                 | 09/22/2025 | 09/22/2025                                | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T3.3      | 3                                                                                                                                                                                    | **Compute - Launch Instance:** <br> - Launch t3.micro instance (Free Tier) <br> - In Public Subnet 1 <br> - Assign Security Group `Web-SG` created in Week 2            | 09/23/2025 | 09/23/2025                                | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T3.4      | 4                                                                                                                                                                                    | **IAM - Role Creation:** <br> - Create IAM Role `EC2-S3-Access-Role` <br> - Policy: `AmazonS3ReadOnlyAccess` <br> - Trust entity: `ec2.amazonaws.com`                   | 09/24/2025 | 09/24/2025                                | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T3.5      | 4                                                                                                                                                                                    | **Compute - Attach Role:** <br> - Attach IAM Role to running instance <br> - Via Actions > Security > Modify IAM Role                                                   | 09/24/2025 | 09/25/2025                                | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T3.6      | 5                                                                                                                                                                                    | **CLI - Verification:** <br> - SSH into instance <br> - Install AWS CLI (if not available) <br> - Run `aws s3 ls` to verify access                                      | 09/25/2025 | 09/26/2025                                | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T3.7      | 6                                                                                                                                                                                    | **Storage - EBS Operations:** <br> - Create 1GB gp3 EBS volume in same AZ as instance <br> - Attach to instance <br> - Use `lsblk`, `mkfs -t xfs`, and `mount` commands | 09/26/2025 | 09/28/2025                                | Completed | <https://cloudjourney.awsstudygroup.com/> |

### Week 3 Achievements:

- **Operational Infrastructure:**

  - First Web server is online with Public IP
  - Accessible via secure SSH
  - Clear understanding of differences between Instance Types (T3, C5, R5)

- **Application Security:**

  - Demonstrated EC2 can access S3 Buckets without `aws configure`
  - No need to store Access Keys on server
  - Applied "Temporary Credentials" mechanism through IAM Role

- **Storage:**

  - Understanding difference between EBS (persistent) and Instance Store (ephemeral)
  - Practiced attaching and mounting EBS volume
  - Know how to format and use new disk

- **Troubleshooting:**

  - Initially encountered "Connection Timeout" error when SSH
  - Cause: Forgot to add Inbound Port 22 rule in Security Group
  - Fixed and learned troubleshooting experience

- **Skills:**
  - Proficient in launching and managing EC2 instances
  - Understanding of instance lifecycle (Launch, Stop, Start, Terminate)
  - Solid grasp of Instance Profiles and IAM Roles for EC2 concepts
