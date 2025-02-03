# 📌 GCP Setup Guide

## **1️⃣ Setting Up a GCP Account**
### 📌 Steps:
1. Go to [Google Cloud Platform](https://cloud.google.com/).
2. Click **Get Started for Free**.
3. Sign in with your Google Account.
4. Enter billing details to activate the account (free $300 credit included).
5. Access the **Google Cloud Console**.

---

## **2️⃣ Setting Up IAM Roles**
### 📌 Why IAM?
IAM in GCP allows you to control who has access to specific resources and what actions they can perform.

### 📌 Steps:
1. Go to **IAM & Admin** in the Cloud Console.
2. Click **Create Role**.
   - Specify the role name and description.
   - Add permissions (e.g., `storage.admin` for S3-like bucket management).
3. Assign the role to a user or service account.

---

## **3️⃣ Launching a Virtual Machine (VM)**
### 📌 Steps:
1. Go to **Compute Engine** > **VM Instances**.
2. Click **Create Instance**.
3. Configure:
   - **Machine Type**: Choose a small instance (e.g., `e2-micro` for Free Tier).
   - **Boot Disk**: Use a standard image like Ubuntu or Debian.
   - **Firewall Rules**: Allow HTTP/HTTPS or custom ports.
4. Click **Create** to launch the instance.

---

## **4️⃣ Creating a Cloud Storage Bucket**
### 📌 Steps:
1. Go to **Cloud Storage** in the Cloud Console.
2. Click **Create Bucket**.
3. Configure:
   - **Name**: Provide a unique bucket name.
   - **Location Type**: Multi-region or Regional.
   - **Storage Class**: Standard, Nearline, Coldline, or Archive.
4. Click **Create**.

---

## **5️⃣ Networking Basics in GCP**
### 📌 VPC Setup:
1. Go to **VPC Network** > **VPC Networks**.
2. Create a new VPC:
   - **Name**: `custom-vpc`
   - **Subnet**: Provide a CIDR range (e.g., `10.0.0.0/16`).
3. Add Subnets:
   - Public Subnet: `10.0.1.0/24`
   - Private Subnet: `10.0.2.0/24`.
4. Configure Firewall Rules:
   - Allow SSH, HTTP, or custom traffic.

---

## **6️⃣ Hands-On Exercises**
💻 **Tasks:**
1. Create a GCP VM, configure SSH, and install Nginx.
2. Create a Cloud Storage bucket and upload files.
3. Design a custom VPC with multiple subnets.

---
