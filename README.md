AWS VPC with Public and Private Subnets

📌 Project Overview

This project demonstrates how to create a custom Amazon VPC with public and private subnets, configure an Internet Gateway, and manage traffic using route tables.
It follows AWS best practices for network isolation and secure architecture.

-------------------------------------------------------------------------------

🛠️ Services Used

Amazon VPC

Subnets

Internet Gateway (IGW)

Route Tables

Amazon EC2 (for testing)

------------------------------------------------------------------------------------

🏗️ Architecture

The architecture includes:

One custom VPC

One public subnet (with internet access)

One private subnet (without direct internet access)

Internet Gateway attached to the VPC

Separate route tables for public and private subnets

Public Subnet

Used for internet-facing resources (e.g., web servers)

Connected to the Internet Gateway

Private Subnet

Used for backend resources (e.g., databases)

No direct internet access

-------------------------------------------------------------------------------------------

🧱 VPC Configuration Details

ResourceConfigurationVPC CIDR10.0.0.0/16Public Subnet CIDR10.0.1.0/24Private Subnet CIDR10.0.2.0/24Regionap-south-1 (Mumbai)

----------------------------------------------------------------------------------------------------------

🚀 Step-by-Step Implementation

1. Create a VPC

CIDR block: 10.0.0.0/16

Name: My-VPC

2. Create Subnets

Public Subnet: 10.0.1.0/24

Private Subnet: 10.0.2.0/24

3. Create and Attach Internet Gateway

Create IGW

Attach it to the VPC

4. Configure Route Tables

Public Route Table

Route: 0.0.0.0/0 → Internet Gateway

Associated with Public Subnet

Private Route Table

Only local route

Associated with Private Subnet

5. Enable Public IP for Public Subnet

Auto-assign public IPv4 address enabled

--------------------------------------------------------------------------------------------

✅ Verification & Testing

Public Subnet Test

Launch EC2 in Public Subnet

Instance receives public IP

Internet access works (SSH / ping / browser)

Private Subnet Test

Launch EC2 in Private Subnet

No public IP assigned

Internet access not available

✔ This confirms correct VPC configuration.

--------------------------------------------------------------------------------------

🔐 Security Best Practices

Network isolation using private subnets

Controlled internet access via route tables

Separate routing for public and private resources

-----------------------------------------------------------------------------------

📸 Screenshots

Screenshots of the following are included:

VPC details

Subnets

Route tables

Internet Gateway

EC2 connectivity test

-----------------------------------------------------------------------------------

📚 Learning Outcomes

Understanding VPC networking

Difference between public and private subnets

Route table configuration

Internet Gateway usage

Real-world AWS network design

-------------------------------------------------------------------------------------------

🧾 Use Cases

Hosting web applications

Secure backend infrastructure

Foundation for ALB, Auto Scaling, and NAT Gateway

----------------------------------------------------------------------------------------

👤 Author

Dharani Boominathan
AWS Learner | Cloud Enthusiast



