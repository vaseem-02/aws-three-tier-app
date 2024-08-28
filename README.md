# # AWS Robust Web Application Project:
Challenge


## Situation
A robust and scalable web application architecture needed to be designed and implemented on AWS, incorporating best practices for high availability, security, and performance.

## Task
Design and implement a three-tier web application architecture on AWS, including:
1. Network infrastructure with public and private subnets
2. Web servers with load balancing
3. Application servers with PHP and phpMyAdmin
4. Database tier using Amazon RDS

## Action
1. Network Setup:
   - Created VPC "awsProject-vpc" with CIDR 20.0.0.0/20
   - Set up 2 public and 4 private subnets across 2 AZs
   - Configured NAT Gateway, Internet Gateway, and route tables

2. Compute Layer:
   - Launched EC2 instances: 1 jump server, 2 application servers
   - Configured security groups for each tier

3. Application Setup:
   - Installed and configured Apache, PHP 8.2, and phpMyAdmin on app servers
   - Set up Application Load Balancer with target groups

4. Database Layer:
   - Created RDS MySQL instance in private subnets
   - Configured database security group

5. Integration:
   - Connected phpMyAdmin to RDS instance
   - Enabled sticky sessions on ALB

## Result
- Successfully implemented a scalable, highly available 3-tier web application
- Achieved security through network isolation and proper security group configuration
- Implemented load balancing for improved performance and availability
- Established secure database access from application servers
- Created a fully functional web application with database management capabilities

Key Achievements:
- Multi-AZ deployment for high availability
- Secure bastion host setup for management
- Proper use of public and private subnets
- Functional load balancing with sticky sessions
- Secure database setup with limited access
