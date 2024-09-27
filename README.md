# AWS-3-Tier

## Description: 
In this architecture, a public-facing Application Load Balancer forwards client traffic to our web tier EC2 instances. The web tier is running Nginx webservers that are configured to serve a React.js website and redirects our API calls to the application tier’s internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to our web tier. Load balancing, health checks and autoscaling groups are created at each layer to maintain the availability of this architecture.

## Architecture Overview
![image](https://github.com/user-attachments/assets/be6fec3b-b47a-4554-a111-24a8f17cb944)
  

## Pre-requisites:
1. Set up an AWS account: If you don’t already have one, you can create an AWS account by following the instructions provided [here](https://aws.amazon.com/console/). Click the “Create an AWS Account” button located in the top right corner of the page to begin the process.
2. Choose your preferred IDE or text editor: Select any development environment or text editor that you are comfortable with for writing and editing code.

## Features:
1. **Scalable Design:** Built to easily scale using AWS services such as Auto Scaling and Elastic Load Balancing (ELB) to handle varying workloads efficiently.
2. **Infrastructure Automation:** Utilizes Infrastructure as Code (IaC) tools like AWS CloudFormation or Terraform to automatically provision and manage resources like EC2 instances, RDS, S3, and VPC.
3. **High Availability:** Ensures continuous availability with a multi-AZ (Availability Zone) configuration for both the application and database, providing redundancy and fault tolerance.
4. **Enhanced Security:** Employs AWS IAM roles, Security Groups, and Network ACLs to enforce strong security measures for communication and data protection.

## AWS Services Used
1. Amazon EC2: For hosting the application layer.
2. Amazon RDS: To manage the relational database.
3. Amazon S3: For static file storage.
4. Amazon VPC: For network isolation and security.
5. Amazon Route 53: For DNS routing.
6. Elastic Load Balancing (ELB): For distributing traffic across instances.
7. AWS Auto Scaling: To dynamically scale resources based on traffic.
