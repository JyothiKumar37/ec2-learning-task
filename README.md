EC2 Provisioning: Manual (AWS Console) & Terraform (IaC)
Project Overview

This repository demonstrates my learning and hands-on experience in provisioning an EC2 (Elastic Compute Cloud) instance using two different approaches:
Manual provisioning using AWS Management Console

Automated provisioning using Terraform (Infrastructure as Code)

The objective of this task is to understand AWS EC2 fundamentals, compare manual vs automated infrastructure provisioning, and follow DevOps best practices by maintaining clean, version-controlled infrastructure code.

 Tools & Technologies Used

Amazon Web Services (EC2)

Terraform

Git & GitHub

Linux

 EC2 Creation Using AWS Console (Manual Method)
Description

In this approach, the EC2 instance was created manually using the AWS Management Console.
This helped in understanding core AWS concepts and the console-based workflow.

 High-Level Steps

Logged in to AWS Console

Navigated to EC2 service

Selected Amazon Linux 2 AMI

Chose t2.micro instance type

Configured key pair and security group

Launched the EC2 instance

Screenshots

Screenshots documenting the step-by-step EC2 creation process are stored in the screenshots/ directory.


screenshots/
├── p4.png
├── p5.png
├── p6.png
├── p7.png
└── p8.png



These screenshots capture:

Instance configuration

AMI and instance type selection

Security group rules

Successful EC2 launch

 Learnings from Manual Approach

Understanding of AMI, instance types, and key pairs

Role of security groups as virtual firewalls

How EC2 instances get public IP addresses

Manual provisioning is good for learning but not scalable

EC2 Creation Using Terraform (Infrastructure as Code)
Description

In this approach, EC2 infrastructure was provisioned using Terraform.
Terraform enables defining infrastructure as code, making it automated, reusable, and version-controlled.

 Terraform Directory Structure

 
terraform-ec2/
├── provider.tf
├── variables.tf
├── main.tf
├── security_group.tf
├── outputs.tf
└── terraform.tfvars



 Purpose of Each File

provider.tf → Configures AWS provider and region

variables.tf → Declares reusable input variables

main.tf → Defines the EC2 instance resource

security_group.tf → Configures EC2 security group rules

outputs.tf → Displays EC2 details after creation

terraform.tfvars → Stores actual values for variables (AMI ID, key name, etc.)

 Terraform Workflow Used
terraform init
terraform fmt
terraform validate
terraform plan
terraform apply


To clean up resources:

terraform destroy

 Learnings from Terraform Approach

Infrastructure as Code (IaC concepts)

Separation of configuration and values using terraform.tfvars

Terraform lifecycle and execution flow

Automated and repeatable EC2 provisioning

Reduced manual errors

Easy infrastructure cleanup




Key Takeaways

Manual EC2 creation helps understand AWS fundamentals

Terraform is essential for real-world DevOps workflows

terraform.tfvars improves security and reusability

Infrastructure as Code ensures consistency and scalability

GitHub helps track and manage infrastructure changes

Conclusion:

This project provided hands-on experience with both manual EC2 provisioning and automated provisioning using Terraform.
While manual setup is suitable for learning, Terraform is the preferred approach in production environments due to automation, consistency, and maintainability.
