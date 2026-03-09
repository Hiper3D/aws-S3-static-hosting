# ☁️ AWS Cloud Infrastructure: Static Website Deployment

![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-web-services&logoColor=white)
![Amazon S3](https://img.shields.io/badge/Amazon%20S3-569A31?style=for-the-badge&logo=Amazon%20S3&logoColor=white)
![IAM](https://img.shields.io/badge/AWS%20IAM-DD344C?style=for-the-badge&logo=amazonwebservices&logoColor=white)

## 📋 Project Overview
This repository serves as the **Infrastructure Documentation** for my personal portfolio website. To demonstrate practical cloud engineering skills, I decoupled the application code from its hosting environment. I migrated the deployment from a fully managed PaaS (Platform as a Service - a cloud computing model that provides a platform allowing customers to develop, run, and manage applications) to custom AWS (Amazon Web Services - a comprehensive cloud computing platform) infrastructure.

🔗 **[Click Here to View the Application Source Code]** *(Note: Replace this text with the link to your old Vercel code repo!)*

## 🚀 Live Environment
* **Current S3 Endpoint:** [Portfolio Live Site](http://first-demo-757038.s3-website.ap-south-1.amazonaws.com) 
* *Note: The site is currently served via HTTP (Hypertext Transfer Protocol - the foundation of data communication for the World Wide Web). HTTPS (Hypertext Transfer Protocol Secure - a secure communication protocol) implementation is pending AWS account verification for CDN (Content Delivery Network - a geographically distributed network of servers to deliver content faster) provisioning.*

## 🏗️ Architecture & Security Implementations

### 1. Storage & Hosting
* Provisioned an **Amazon S3 (Simple Storage Service - an object storage service offering high scalability and security)** bucket configured specifically for static website hosting.
* Deployed resources in the `ap-south-1` (Mumbai) region to ensure optimal latency for regional traffic across India.

### 2. Identity & Access Management
* **Modernized Security:** Enforced strict security baselines by permanently disabling legacy ACLs (Access Control Lists - older, less secure rules that specify which users can access individual files) using the "Bucket Owner Enforced" setting.
* **Custom Bucket Policies:** Authored and attached a custom JSON (JavaScript Object Notation - a lightweight data-interchange format) bucket policy granting `s3:GetObject` permissions. This securely manages public read access to web assets while protecting the underlying bucket architecture.

## 🗺️ Roadmap & Next Steps
To elevate this infrastructure to production-grade, the following implementations are planned once AWS support lifts the new-account service restrictions:
* **Global Caching:** Deploy an AWS CloudFront distribution to serve as a global CDN, drastically reducing latency for international visitors.
* **Traffic Encryption:** Provision a free SSL/TLS (Secure Sockets Layer/Transport Layer Security - standard technologies for keeping an internet connection secure) certificate via AWS ACM (AWS Certificate Manager - a service that lets you easily provision, manage, and deploy public and private SSL/TLS certificates) to enforce HTTPS routing.
* **Custom DNS Routing:** Map a custom professional domain to the CloudFront distribution.

---
*Built by Priyanshu Patra | Aspiring Cloud & Network Engineer*
