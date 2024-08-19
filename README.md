# Setting up AWS Infrastructure using Terraform

## Project Description
This project demonstrates the use of **Infrastructure as Code (IaC)** principles to automate the setup and management of AWS infrastructure using **Terraform**. The goal is to create a scalable, secure, and efficient cloud environment by defining and provisioning AWS resources in a repeatable and consistent manner.

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

5. **Apply the Terraform Configuration**:
    Apply the changes to create the AWS infrastructure:
    ```bash
    terraform apply
    ```
    Confirm the action when prompted.

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
