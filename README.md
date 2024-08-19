# Setting up AWS Infrastructure using Terraform

## Project Description
This project demonstrates the use of **Infrastructure as Code (IaC)** principles to automate the setup and management of AWS infrastructure using **Terraform**. The goal is to create a scalable, secure, and efficient cloud environment by defining and provisioning AWS resources in a repeatable and consistent manner.

## Project Architecture
![image](https://github.com/user-attachments/assets/38b710b6-5495-4e3b-8049-fff6ce651577)


## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Project Architecture](#project-architecture)
- [Prerequisites](#prerequisites)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Best Practices](#best-practices)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction
Terraform is a powerful tool for defining cloud infrastructure in a declarative manner. By utilizing Terraform with AWS, you can manage resources such as VPCs, subnets, route tables, security groups, EC2 instances, and load balancers with ease and reliability. This project serves as an introduction to Terraform and showcases how to use it to automate the provisioning of AWS infrastructure.

## Features
- **Automated VPC and Subnet Creation**: Automatically set up a Virtual Private Cloud (VPC) with subnets to segment your network.
- **Route Tables Configuration**: Create and associate route tables for efficient routing within your AWS network.
- **Security Groups Setup**: Define and configure security groups to control inbound and outbound traffic for your resources.
- **EC2 Instances with Load Balancing**: Provision multiple EC2 instances and use scripts to ensure they are load-balanced.
- **Application Load Balancer**: Set up an Application Load Balancer (ALB) to distribute incoming traffic across multiple EC2 instances.
- **Comprehensive AWS Resource Management**: Use Terraform to manage and automate the creation, updating, and deletion of AWS resources.

## Project Architecture
The project is structured to automate the setup of a complete AWS infrastructure. Below are the key components:

1. **VPC and Subnets**: A VPC is created with public and private subnets to segment the environment.
2. **Route Tables**: Route tables are defined and associated with the respective subnets for proper network routing.
3. **Security Groups**: Security groups are set up to control access to the EC2 instances and other AWS resources.
4. **EC2 Instances**: Multiple EC2 instances are provisioned, and scripts are applied to facilitate load balancing.
5. **Application Load Balancer (ALB)**: An ALB is created to distribute traffic across the EC2 instances.
6. **Resource Management**: Terraform is used to manage the entire lifecycle of AWS resources, ensuring consistency and scalability.

## Prerequisites
Before you begin, ensure you have the following installed:

- **Terraform** (version 0.12+)
- **AWS CLI** configured with your credentials
- An **AWS Account** with appropriate permissions to create and manage resources

## Setup Instructions
1. **Clone the Repository**:
    ```bash
    git clone https://github.com/yourusername/Setting-up-AWS-Infrastructure-using-Terraform.git
    cd Setting-up-AWS-Infrastructure-using-Terraform
    ```

2. **Configure AWS CLI**:
    Make sure your AWS CLI is configured with access keys. If not, run:
    ```bash
    aws configure
    ```
    Enter your AWS Access Key, Secret Key, region, and output format when prompted.

3. **Initialize Terraform**:
    ```bash
    terraform init
    ```

4. **Plan the Infrastructure**:
    Generate an execution plan to preview changes:
    ```bash
    terraform plan
    ```
![WhatsApp Image 2024-08-15 at 17 27 04_0ebe21a7](https://github.com/user-attachments/assets/22d29385-675d-428e-833c-2b418ea74c83)
![WhatsApp Image 2024-08-15 at 17 27 24_0f70a09b](https://github.com/user-attachments/assets/b1854d3b-3349-4fed-863a-348bf43c342d)



5. **Apply the Terraform Configuration**:
    Apply the changes to create the AWS infrastructure:
    ```bash
    terraform apply
    ```
    Confirm the action when prompted.
![WhatsApp Image 2024-08-15 at 17 27 51_2749680c](https://github.com/user-attachments/assets/c161f7a2-617c-4dea-9171-9194f0865964)
![WhatsApp Image 2024-08-15 at 17 28 13_dcbc610d](https://github.com/user-attachments/assets/24fbf06a-1a5f-4e0b-a519-4fcc91ac7b25)




6. **Verify the Setup**:
    After the `terraform apply` command completes, you can verify the AWS resources created through the AWS Management Console.

## Usage
After setting up the infrastructure, you can manage it by modifying the Terraform configuration files. To apply changes, simply run:
```bash
terraform apply
```

To destroy the infrastructure when no longer needed, run:
```
terraform destroy
```

## Screenshots

![WhatsApp Image 2024-08-15 at 15 28 06_bfb06bc4](https://github.com/user-attachments/assets/e03ae153-623a-454e-9d4c-d2f7760c50d7)
![WhatsApp Image 2024-08-15 at 15 28 35_90556ef0](https://github.com/user-attachments/assets/e4fbff9e-7eb5-46a9-89cc-fdeb33a25362)
![WhatsApp Image 2024-08-15 at 15 28 47_fa536dc8](https://github.com/user-attachments/assets/6ff3b3cc-be7d-4c14-92c3-79b693f169f5)
![WhatsApp Image 2024-08-15 at 15 29 04_74abfd22](https://github.com/user-attachments/assets/ff920de7-eaf7-401f-990f-65bbf013011d)
![WhatsApp Image 2024-08-15 at 15 29 20_7cc805a3](https://github.com/user-attachments/assets/59ab6850-7884-4e21-890c-42a0b0a179c5)
![WhatsApp Image 2024-08-15 at 15 29 33_5dd5d1fa](https://github.com/user-attachments/assets/067de682-0f8c-482b-872b-052875693ed2)
![WhatsApp Image 2024-08-15 at 15 29 46_538d1f25](https://github.com/user-attachments/assets/408e7e67-4573-4dea-abff-d978591039c3)
![WhatsApp Image 2024-08-15 at 15 29 55_18a457a1](https://github.com/user-attachments/assets/cd7e8fc0-23fa-494e-a7e6-afbfb3b83aa9)
![WhatsApp Image 2024-08-15 at 15 30 08_8d0c1104](https://github.com/user-attachments/assets/dd0d81d0-37a3-427b-b200-2324b69d0fb9)
![WhatsApp Image 2024-08-15 at 15 30 20_62dc1b86](https://github.com/user-attachments/assets/6eccc345-52c1-479d-a23c-a3ed45df35bf)

## Final Output 
![WhatsApp Image 2024-08-15 at 15 27 08_1698c72b](https://github.com/user-attachments/assets/4efff46a-1def-43de-a88a-664776b93b24)
![WhatsApp Image 2024-08-15 at 15 27 32_73318993](https://github.com/user-attachments/assets/8eb50321-587a-492a-9974-ff6da0a90828)












