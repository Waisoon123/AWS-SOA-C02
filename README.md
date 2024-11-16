# AWS-SOA-C02
This repository contains a comprehensive cheatsheet and mini projects aimed at building and enhancing sysops skills, designed specifically to support preparation for the AWS-SOA-C02 certification exam.

## Exam Domains
+ Domain 1: Monitoring, Logging, and Remediation **20%**
+ Domain 2: Reliability and Business Continuity **16%**
+ Domain 3: Deployment, Provisioning, and Automation **18%**
+ Domain 4: Security and Compliance **16%**
+ Domain 5: Networking and Content Delivery **18%**
+ Domain 6: Cost and Performance Optimization **12%**

### Domain 1: Monitoring, Logging, and Remediation
Task Statement 1.1: Implement metrics, alarms, and filters by using AWS monitoring and logging services.
+ Identify, collect, analyze, and export logs (E.g., Amazon CloudWatch Logs, CloudWatch Logs Insights, AWS CloudTrail Logs).
+ Collect metrics and logs by using the CloudWatch agent.
+ Create CloudWatch alarms.
+ Create metric filters.
+ Create CloudWatch dashboards.
+ Configure notifications (E.g., Amazon Simple Notification Service, Service Quotas, CloudWatch alarms, AWS Health events).

Task Statement 1.2: Remediate issues based on monitoring and availability metrics. 
+ Troubleshoot or take corrective actions based on notifications and alarms.
+ Configure Amazon EventBridge rules to invoke actions.
+ Use AWS Systems Manager Automation runbooks to take action based on AWS Config rules.

### Domain 2: Reliability and Business Continuity
Task Statement 2.1: Implement scalability and elasticity.
+ Create and maintain AWS Auto Scaling plans.
+ Implement caching.
+ Implement AWS RDS replicas and AWS Aurora Replicas.
+ Implement loosely coupled architectures.
+ Differentiate between horizontal scaling and vertical scaling.

Task Statement 2.2: Implement high availability and resilient environments. 
+ Configure ELB and AWS Route 53 health checks.
+ Differentiate between the use of a single Availability Zone and Multi-AZ deployments (E.g., AWS EC2 Auto Scaling groups, ELB, AWS FSx, AWS RDS).
+ Implement fault-tolerant workloads (E.g., AWS EFS, Elastic IP addresses).
+ Implement Route 53 routing policies (E.g., Failover, weighted, latency based).

Task Statement 2.3: Implement backup and restore strategies.
+ Automate snapshots and backups based on use cases (E.g., RDS snapshots, AWS Backup, RTO and RPO, AWS Data Lifecycle Manager, retention policy).
+ Restore databases (E.g., Point-in-time restore, promote read replica).
+ Implement versioning and lifecycle rules.
+ Configure AWS S3 Cross-Region Replication
+ Perform disaster recovery procedures.

### Domain 3: Deployment, Provisioning, and Automation
Task Statement 3.1: Provision and maintain cloud resources
+ Create and manage AMIs (E.g., EC2 Image Builder)
+ Create, manage, and troubleshoot AWS CloudFormation.
+ Provision resources across multiple AWS Regions and accounts (E.g., AWS Resource Access Manger, CloudFormation StackSets, IAM Cross-Account roles).
+ Select deployment scenarios and services (E.g., Blue/Green, rolling, canary).
+ Identify and remediate deployment issues (E.g., service quotas, subnet sizing, CloudFormation errors, permissions).

Task Statement 3.2: Automate manual or repeatable processes. 
+ Use AWS Services (E.g., Systems Manager, CloudFormation) to automate deployment processes.
+ Implement Automated patch management.
+ Schedule automated tasks by using AWS services (E.g., EventBrdige, AWS Config).

### Domain 4: Security and Compliance
Task Statement 4.1: Implement and manage security and compliance policies. 
+ Implement IAM features (E.g., password policies, multi-factor authentication, roles, SAML, federated identity, resource policies, policy conditions).
+ Troubleshoot and audit access issues by using AWS services (E.g., CloudTrail, IAM Access Analyzer, IAM policy simulator).
+ Validate service control policies (SCPs) and permissions boundaries
+ Review AWS Trusted Advisor security checks.
+ Validate AWS Region and service selections based on compliance requirements. 
+ Implement secure multi-account strategies (E.g., AWS Control Tower, AWS Organizations)

Task Statement 4.2: Implement data and infrastructure protection strategies.
+ Enforce a data classification scheme.
+ Create, manage, and protect encryption keys.
+ Implement encryption at rest (E.g., AWS Key Management Service)
+ Implement encryption in transit (E.g., AWS Certificate Manager, VPN)
+ Securely store secrets by using AWS services (E.g., AWS Secrets Manager, Systems Manager Parameter Store)
+ Review reports or findings (E.g., AWS Security Hub, Amazon GuardDuty, AWS Config, Amazon Inspector)

### Domain 5: Networking and Content Delivery
Task Statement 5.1: Implement networking features and connectivity. 
+ Configure a VPC (E.g., subnets, route tables, network ACLs, security groups, NAT gateway, internet gateway).
+ Configure private connectivity (E.g., Systems Manager Session Manager, VPC endpoints, VPC peering, VPN).
+ Configure AWS network protection services (E.g., AWS WAF, AWS Shield)

Task Statement 5.2: Configure domains, DNS services, and content delivery.
+ Configure Route 53 hosted zones and records.
+ Implement Route 53 routing policies (for example, geolocation, geoproximity).
+ Configure DNS (for example, Route 53 Resolver).
+ Configure Amazon CloudFront and S3 origin access control (OAC).
+ Configure S3 static website hosting.

Task Statement 5.3: Troubleshoot network connectivity issues.
+ Interpret VPC configurations (E.g., subnets, route tables, network ACLs, security groups).
+ Collect and interpret logs (E.g., VPC Flow Logs, ELB access logs, AWS WAF web ACL logs, CloudFront logs).
+ Identify and remediate CloudFront caching issues.
+ Troubleshoot hybrid and private connectivity issues.

### Domain 6: Cost and Performance Optimization
Task Statement 6.1: Implement cost optimization strategies.
+ Implement cost allocation tags.
+ Identify and remediate underutilized or unused resources by using AWS services and tools (E.g., Trusted Advisor, AWS Compute Optimizer, AWS Cost Explorer).
+ Configure AWS Budgets and billing alarms.
+ Assess resource usage patterns to qualify workloads for EC2 Spot Instances.
+ Identify opportunities to use managed services (for example, Amazon RDS, AWS Fargate, Amazon EFS). 

Task Statement 6.2: Implement performance optimization strategies.
+ Recommend compute resources based on performance metrics.
+ Monitor Amazon Elastic Block Store (Amazon EBS) metrics and modify configuration to increase performance efficiency.
+ Implement S3 performance features (E.g., S3 Transfer Acceleration, multipart uploads).
+ Monitor RDS metrics and modify the configuration to increase performance efficiency (E.g., Performance Insights, RDS Proxy).
+ Enable enhanced EC2 capabilities (for example, Elastic Network Adapter, instance store, placement groups).

### Resources:
+ https://d1.awsstatic.com/training-and-certification/docs-sysops-associate/AWS-Certified-SysOps-Administrator-Associate_Exam-Guide.pdf
