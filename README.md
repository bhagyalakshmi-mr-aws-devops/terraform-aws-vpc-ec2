# Terraform AWS VPC + EC2 Infrastructure Project

This project demonstrates Infrastructure as Code (IaC) using Terraform to provision a complete AWS networking and compute setup in a production-aligned manner.

---

## 🚀 What This Project Does

Using Terraform, this project automatically creates:

- A custom AWS VPC
- Internet Gateway for public access
- Public subnet with routing
- Route table and association
- Security Group with controlled inbound rules
- EC2 instance running Amazon Linux
- NGINX web server installed via user_data

Once deployed, the EC2 instance serves a live web page confirming successful infrastructure provisioning.

---

## 🏗️ Architecture Overview

- **VPC** – Isolated AWS network
- **Public Subnet** – Hosts the EC2 instance
- **Internet Gateway** – Enables internet access
- **Route Table** – Routes traffic externally
- **Security Group**
  - HTTP (80) open to the internet
  - SSH (22) restricted to user IP
- **EC2 Instance**
  - Amazon Linux 2023
  - NGINX installed automatically

---

## 🛠️ Tech Stack

- Terraform
- AWS EC2
- AWS VPC
- Amazon Linux
- NGINX
- Linux
- Git & GitHub

---

## 📂 Project Structure
terraform-aws-vpc-ec2/
│── main.tf
│── provider.tf
│── variables.tf
│── outputs.tf
│── terraform.tfvars
│── versions.tf
│── .gitignore
│── README.md


---

How to Run

Initialize Terraform:
terraform init

Validate and generate the execution plan:
terraform validate
terraform plan

Apply the infrastructure:
terraform apply -auto-approve


Outputs

After a successful deployment, Terraform will output the following values:
VPC ID
Subnet ID
EC2 Public IP
Public URL to access the NGINX web server

Example:
http://<EC2_PUBLIC_IP>


Cleanup

To destroy all created AWS resources:
terraform destroy -auto-approve

