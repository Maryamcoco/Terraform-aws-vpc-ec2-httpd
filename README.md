 # 🌍 Terraform AWS Webserver Deployment  

![Terraform](https://img.shields.io/badge/IaC-Terraform-7B42BC?style=flat&logo=terraform)  
![AWS](https://img.shields.io/badge/Cloud-AWS-FF9900?style=flat&logo=amazonaws)  
![DevOps](https://img.shields.io/badge/Practice-DevOps-2496ED?style=flat&logo=docker)  

---

## 📖 Project Overview  

This project demonstrates **Infrastructure as Code (IaC)** using **Terraform** to provision a highly available **AWS EC2 instance** running a simple web server (`httpd`).  

It reflects real-world DevOps practices: **version-controlled infrastructure, modular design, and automated provisioning**.  
The repo is structured as if it were part of a larger production-ready infrastructure portfolio.  

---

## 🎯 Objectives  

- ✅ Use Terraform to define and provision AWS resources.  
- ✅ Deploy an EC2 instance inside a **custom VPC**.  
- ✅ Configure **security groups** for HTTP/SSH access.  
- ✅ Automate installation of **Apache httpd** web server.  
- ✅ Output the **public IP address** of the instance.  

---

## 🏗️ Architecture  
            ┌───────────────────────┐
            │       Internet        │
            └─────────┬─────────────┘
                      │
                ┌─────▼─────┐
                │  AWS VPC  │
                └─────┬─────┘
                      │
               ┌──────▼──────┐
               │  Subnet     │
               └──────┬──────┘
                      │
            ┌─────────▼─────────┐
            │  EC2 Instance     │
            │  (httpd server)   │
            └───────────────────┘

---

## 🛠️ Tech Stack  

- **Terraform** (IaC automation)  
- **AWS EC2** (compute)  
- **AWS VPC & Subnet** (networking)  
- **AWS Security Group** (firewall)  
- **Apache httpd** (web server)  

---

## 📂 Repository Structure  
 aws-terraform-webserver/
│── main.tf # Core infrastructure definition (EC2, SG, etc.)
│── provider.tf # Provider configuration (AWS region, profile)
│── output.tf # Output values (public IP, DNS)
│── variables.tf # Input variables (instance type, AMI, etc.)
│── .gitignore # Ignore Terraform state files & secrets
└── README.md # Project documentation

---

## 🚀 Deployment Guide  

### 1️⃣ Clone Repository  
```
git clone https://github.com/Maryamcoco/Terraform-aws-vpc-ec2-httpd.git
```
 cd Terraform-aws-vpc-ec2-httpd
 
2️⃣ Initialize Terraform
```
 terraform init
```
3️⃣ Review Execution Plan
```
 terraform plan
```
4️⃣ Apply Configuration
```
 terraform apply -auto-approve
```
5️⃣ Retrieve Public IP
--terraform output aws_instance_public_ip copy and paste the output it gave you on your browser
Open browser → http://<PUBLIC_IP> → Apache default page should load 🎉

---
🔒 Security Considerations

-Sensitive values (keys, state files) excluded via .gitignore.

-Remote backend (e.g., S3 + DynamoDB) recommended for production state mgmt.

-Security groups restricted to **SSH (22) and HTTP (80)**.

---
📊 Key Learnings

-Infrastructure reproducibility using **Terraform IaC**.

-Importance of idempotent **infrastructure** (apply doesn’t duplicate).

-Applying **GitOps best practices** by version-controlling infra configs.

---
## 🚀 Future Enhancements  

🔹 **Add `variables.tf` file** → To parameterize values such as instance type, region, VPC CIDR, and AMI for better flexibility.  
🔹 **Introduce Load Balancer (ALB/ELB)** → For high availability and fault tolerance.  
🔹 **Use Terraform Modules** → To organize and reuse infrastructure components.  
🔹 **Integrate CI/CD pipeline** → Automate Terraform plan & apply using GitHub Actions or Jenkins.  
🔹 **Multi-Cloud Support** → Extend infrastructure to AWS, Azure, and GCP for hybrid-cloud setups.  

----
## 👩‍💻 About Me

I am a **Junior DevOps Engineer** with hands-on experience in:

☁️ Cloud Platforms: **AWS, Azure, GCP**

⚙️ Tools: **Terraform, Docker, Kubernetes, Ansible, Jenkins, GitHub Actions**

📈 Monitoring: **Prometheus, Grafana, SonarCloud, Datadog**

💻 Programming/Scripting: **Python, Bash, Go (learning)**

I build portfolio projects like this to simulate **real-world production setups**, continuously improving my skill set.

📬 **connect with me** at: [LinkedIn](https://www.linkedin.com/in/maryam-temitope-2a3428373/)
 | Email abdulraufmaryam15@gmail.com

✨ This repository is part of my **DevOps engineering portfolio**, showcasing my growth in **Infrastructure as Code and cloud automation**.



