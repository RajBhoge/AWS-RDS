# AWS RDS — Setting Up a Relational Database Instance

A practical guide to provisioning and configuring an **Amazon RDS (Relational Database Service)** instance on AWS, covering database engine selection, security configuration, and ongoing maintenance.

## Overview

Amazon RDS is a managed relational database service that makes it easy to set up, operate, and scale databases in the cloud. This repository walks through launching an RDS instance from scratch — from choosing an engine to connecting your application.

## What's Covered

- Navigating the AWS Console to create an RDS instance
- Choosing a database engine (MySQL, PostgreSQL, Oracle, SQL Server)
- Configuring instance class, storage, and credentials
- Setting up VPC, subnet groups, and security groups
- Connecting an application to the RDS endpoint
- Monitoring performance and managing backups

## Setup Steps

### 1. Open RDS Console
Navigate to **RDS** in the AWS Management Console and click **Create database**.

### 2. Choose Engine
Select your preferred database engine: MySQL, PostgreSQL, Oracle, SQL Server, or Amazon Aurora.

### 3. Configure Instance
- **Instance class** — Choose based on workload (e.g., `db.t3.micro` for dev/test)
- **Storage** — Set allocated storage and enable autoscaling if needed
- **Identifier** — Unique name for your DB instance
- **Credentials** — Set master username and password

### 4. Network & Security
- Assign to a **VPC** with the appropriate subnet group
- Configure **security groups** to allow inbound traffic on the DB port (e.g., 3306 for MySQL)

### 5. Advanced Settings
- **Backup retention** — Set retention period for automated backups
- **Maintenance window** — Schedule for minor version upgrades
- **Enhanced monitoring** — Enable for OS-level metrics

### 6. Connect
Use the endpoint from the RDS dashboard:
```
<db-identifier>.<region>.rds.amazonaws.com:<port>
```

## Technologies

| Service | Purpose |
|---------|---------|
| Amazon RDS | Managed relational database |
| VPC & Security Groups | Network isolation and access control |
| AWS IAM | Permissions and access management |
| CloudWatch | Monitoring and alerting |

## Author

**Raj Bhoge** — Cloud & AI Engineer  
[GitHub](https://github.com/RajBhoge) | [LinkedIn](https://www.linkedin.com/in/raj-bhoge-834280194/) | [Blog](https://rajbhoge2107.hashnode.dev/)
