# Automated Lab 🚀

A **serverless AWS-based platform** that enables users to **create, manage, and destroy Linux, Windows, and Mac EC2 lab environments with a single click**, without accessing the AWS Console.

🌐 **Live App:** [https://nexuslabs.cloudlightcorp.com](https://nexuslabs.cloudlightcorp.com)
📦 **Lambda Repository:** [https://github.com/Cloudlightcorp/nexus-labs-lambda-functions-automation-v1.0.git](https://github.com/Cloudlightcorp/nexus-labs-lambda-functions-automation-v1.0.git)

---

## 🔹 Problem Statement

Manual EC2 lab provisioning involves multiple error-prone steps such as VPC setup, key pair handling, OS selection, password decryption, and cleanup. This process is slow, insecure, and not scalable for multi-user environments.

---

## 🔹 Solution

**Automated Lab** provides a **fully serverless, secure, and scalable automation layer** that allows users to provision and manage EC2 lab environments using a web dashboard, with built-in job tracking, security, and cost control.

---

## 🔹 Key Features

* One-click EC2 provisioning (Linux / Windows / Mac)
* Secure authentication using Amazon Cognito
* Asynchronous job execution with real-time status tracking
* Automated EC2 key pair management (S3 + Secrets Manager)
* Windows password decryption using custom Lambda layer
* Idle instance auto-stop (cost optimization)
* Full user resource cleanup
* Strict IAM least-privilege enforcement

---

## 🔹 High-Level Architecture

<img width="1783" height="738" alt="image" src="https://github.com/user-attachments/assets/6ec8be98-d2e1-4a42-b4d0-dc8b28d03162" />


Backend automation is handled using **EventBridge-triggered Lambdas**.

---

## 🔹 AWS Services Used

* Amazon EC2
* AWS Lambda
* Amazon API Gateway (HTTP API & REST API)
* Amazon S3
* Amazon CloudWatch
* Amazon EventBridge
* AWS Secrets Manager
* Amazon Cognito
* AWS IAM

---

## 🔹 API Design

### HTTP API (Dashboard)

* Cognito-protected
* Used for job submission, job status, instance listing, keypair, and logout

### REST API (Automation)

* API-key protected
* Used for Linux / Windows / Mac EC2 lifecycle operations

---

## 🔹 Security Highlights

* No AWS credentials exposed to frontend
* Cognito-based authentication
* API Gateway authorization before Lambda execution
* User-scoped resource access using tags and S3 prefixes
* Secure key storage using Secrets Manager
* Global logout using Cognito Global Sign-Out

---

## 🔹 Cost Optimization

* Hourly idle instance detection using CloudWatch metrics
* Automatic stop of idle EC2 instances
* Scheduled or manual mass termination support

---

## 🔹 Repository Structure

```
lambda-functions/
├── network/
├── linux/
├── windows/
├── mac/
├── api/
├── cleanup/
└── auth/
```

---

## 🔹 Status

✅ Fully functional
✅ Production-ready
✅ Designed for multi-user environments

---

## 🔹 Author

**Pavithra R.L**
Cloud / DevOps Engineer
Hands-on AWS Automation & Serverless Systems

---


Just tell me.
