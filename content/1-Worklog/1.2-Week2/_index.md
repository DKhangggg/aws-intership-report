---
title: "Week 2 Worklog"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives: Compute and Storage Fundamentals (Sep 15 – Sep 19)

Deploy virtual servers (EC2), understand storage types (EBS, S3), and explore simplified compute models (Lightsail).

### Tasks Completed This Week:

| Day       | Main Activities                                                                                                                                                                      | Date       | Status    | Reference                                 |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------- | ----------------------------------------- |
| Monday    | **Amazon EC2 - Launch & Connect**<br>- Study Compute Essentials<br>- Analyze Instance Types: T3, C5, R5<br>- Select AMI: Amazon Linux 2023<br>- Manage Key Pairs and SSH to instance | 09/15/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| Tuesday   | **Block Storage (EBS) & Windows**<br>- Create and mount EBS volume (gp3)<br>- Deploy Windows Server 2022<br>- Install IIS Web Server<br>- Create Snapshot (incremental backup)       | 09/16/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| Wednesday | **AWS Cloud9 & S3 Basics**<br>- Set up Cloud9 IDE<br>- Study Object Storage model<br>- Configure Static Website Hosting<br>- Write Bucket Policy                                     | 09/17/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| Thursday  | **S3 Advanced & Lightsail**<br>- Set up Lifecycle Policy<br>- Enable Versioning and Encryption<br>- Deploy WordPress on Lightsail                                                    | 09/18/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| Friday    | **Containers on Lightsail**<br>- Package Node.js app as Docker Image<br>- Push to Lightsail Container Service<br>- Familiarize with container workflow                               | 09/19/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |

### Week 2 Achievements:

**Cloud Compute:**

- Mastered EC2 Instance Types and use-cases
- Proficient in Key Pair management and SSH/RDP connections
- Successfully deployed both Linux and Windows workloads
- Understanding of AMI and instance customization

**Block Storage (EBS):**

- Understanding EBS persistence separate from EC2 lifecycle
- Proficient in mounting and managing volumes
- Mastered Snapshot mechanism (incremental backup)
- Differentiated volume types (gp3, io2, st1, sc1)

**Object Storage (S3):**

- Understanding Object Storage model
- Successfully configured Static Website Hosting
- Wrote Bucket Policies with granular permissions
- Implemented Lifecycle Policies for cost optimization
- Applied Security Best Practices (Versioning, Encryption, Block Public Access)

**Development Environment:**

- Using Cloud9 for development workflow
- Eliminated "works on my machine" syndrome
- Secure access without opening SSH ports

**Basic Containers:**

- Familiarized with Docker and containerization
- Successfully deployed application on Lightsail Containers
- Understanding differences between Lightsail and EC2
- Foundation ready for ECS/EKS later

**Application Architecture:**

- Clear separation of compute and storage
- Understanding stateless vs stateful applications
- Ready to build 3-tier architecture next week
