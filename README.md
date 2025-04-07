# IaC-Terraform-Aws-ECS-Fargate-for-Medusa-open-source-headless-commerce-platform-backend


This project provides a complete automation pipeline for deploying the **Medusa e-commerce backend** on AWS using cutting-edge DevOps practices. It leverages **Terraform** for infrastructure provisioning, **Docker** for containerization, **Amazon ECS Fargate (Spot)** for scalable deployments, and **GitHub Actions** for continuous integration and delivery.

---

## 🎯 Project Objectives

- ✅ **Automate Infrastructure Provisioning**  
  Define and manage cloud resources using **Terraform** to ensure reproducibility and scalability.

- 🔁 **CI/CD Pipeline Implementation**  
  Integrate **GitHub Actions** to automate build, test, and deployment workflows.

- 📦 **Application Containerization**  
  Use **Docker** to package Medusa with its dependencies and push the image to **Amazon ECR**.

- ☁️ **Cloud Deployment with AWS**  
  Deploy the containerized app to **AWS ECS (Fargate Spot)** for optimized performance and cost.

- 🔐 **Enhanced Security Practices**  
  Utilize VPCs, subnets, and security groups to ensure secure cloud infrastructure.

---

## 📁 Project Structure

Medusa-ECS-Fargate/
│
├── main.tf             # Terraform configuration
├── variables.tf        # Terraform input variables
├── outputs.tf          # Terraform outputs
├── README.md           # Project documentation
│
└── .github/
    └── workflows/      # GitHub Actions CI/CD workflows


---

## ⚙️ GitHub Actions Workflow Overview

### Trigger  
- 🚨 Triggered on every `push` to the `main` branch.

### Jobs Breakdown

1. **Terraform Infrastructure Provisioning**
   - Sets up VPC, ECS Cluster, ECR repo, RDS, etc.
   - Secrets used: `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, `AWS_REGION`, `DB_PASSWORD`

2. **Pull, Tag, and Push Docker Image**
   - Pulls Medusa image from Docker Hub
   - Tags and pushes it to **Amazon ECR**

3. **Deploy to ECS**
   - Updates the ECS service with the new task definition

4. **Post-Deployment Check**
   - Outputs the RDS endpoint for verification

---

## 🛠️ Technologies Used

| Category         | Tools / Services                   |
|------------------|------------------------------------|
| ☁️ Cloud         | AWS (ECS, ECR, RDS, VPC)           |
| 🏗️ Infrastructure | Terraform                          |
| 🔁 CI/CD         | GitHub Actions                     |
| 📦 Containerization | Docker                            |
| 🧾 Version Control | Git, GitHub                        |
| ⚙️ Config Format | YAML (CI/CD), HCL (Terraform)      |

---

## 🔐 GitHub Secrets Required

- `AWS_ACCESS_KEY_ID`  
- `AWS_SECRET_ACCESS_KEY`  
- `AWS_REGION`  
- `AWS_ACCOUNT_ID`  
- `ECR_REPOSITORY_NAME`  
- `DB_PASSWORD`  
- `ECS_CLUSTER_NAME`  
- `ECS_SERVICE_NAME`  
- `TASK_FAMILY`  

---

## ✅ Result

Successfully automated the CI/CD pipeline for **Medusa Backend**, deployed via **ECS Fargate Spot**, with optimized cloud costs, reusable IaC, and a fully integrated GitHub Actions workflow.  

---

## 👨‍💻 Author

**Bharat Kumar**  
🚀 DevOps & Cloud Enthusiast | CSE Graduate  
📧 gudurubharatkumar8@gmail.com  
🔗 [GitHub](https://github.com/gudurubharatkumar) | [LinkedIn](https://www.linkedin.com/in/gudurubharatkumar)

---

## 💬 Contact

For queries, collaborations, or improvements — feel free to reach out:  
📩 gudurubharatkumar8@gmail.com

---

⭐ **Don't forget to give this project a star if you found it useful!**
