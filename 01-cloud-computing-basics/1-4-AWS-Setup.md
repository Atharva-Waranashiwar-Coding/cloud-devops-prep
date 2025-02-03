# 📌 AWS Setup Guide

## **1️⃣ Setting Up an AWS Account**
### 📌 Steps:
1. Go to [AWS Signup Page](https://aws.amazon.com/).
2. Click **Create a Free Account**.
3. Enter your email, password, and account name.
4. Provide billing information (Credit/Debit card required for verification).
5. Choose the **Free Tier** option for basic usage.
6. Complete identity verification via phone.
7. Log in to the AWS Management Console.

---

## **2️⃣ Setting Up IAM Roles**
### 📌 Why IAM?
IAM (Identity and Access Management) is used to securely control access to AWS services and resources.

### 📌 Steps:
1. Go to the **IAM Service** in the AWS Management Console.
2. Create a **New Role**:
   - Choose a **Trusted Entity**: AWS Service.
   - Select **EC2** as the service.
3. Attach a Policy:
   - Example: Attach `AmazonS3FullAccess` to allow EC2 access to S3.
4. Name the Role and complete the process.

---

## **3️⃣ Launching an EC2 Instance**
### 📌 Steps:
1. Go to the **EC2 Dashboard** in the AWS Console.
2. Click **Launch Instance**.
3. Choose an **Amazon Machine Image (AMI)** (e.g., Amazon Linux 2).
4. Select an **Instance Type** (e.g., `t2.micro` for Free Tier).
5. Configure:
   - **Key Pair**: Create or use an existing one for SSH access.
   - **Security Groups**: Allow traffic (e.g., SSH on port 22, HTTP on port 80).
6. Review and Launch.

---

## **4️⃣ Creating an S3 Bucket**
### 📌 Steps:
1. Go to the **S3 Service** in the AWS Console.
2. Click **Create Bucket**.
3. Provide a unique bucket name.
4. Configure Settings:
   - **Region**: Select a region close to your users.
   - Enable **Versioning** (optional).
5. Complete the setup.

---

## **5️⃣ Networking Basics in AWS**
### 📌 VPC Setup:
1. Go to the **VPC Service**.
2. Create a new **VPC** with a CIDR block (e.g., `10.0.0.0/16`).
3. Create **Subnets**:
   - Public Subnet: `10.0.1.0/24`
   - Private Subnet: `10.0.2.0/24`
4. Configure **Route Tables**:
   - Attach an Internet Gateway to the public subnet.
   - Keep the private subnet isolated.

---

## **6️⃣ Hands-On Exercises**
💻 **Tasks:**
1. Create an EC2 instance, attach an IAM role, and connect to it using SSH.
2. Host a static website using an S3 bucket.
3. Design a VPC with public and private subnets.

---
