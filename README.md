# AWS RDS MySQL Provisioning with Terraform

This project provisions a production-ready AWS RDS MySQL database within private subnets using Infrastructure as Code (IaC) with Terraform.

## 🏗️ Architecture Overview

The infrastructure includes:
- **Custom VPC** with DNS hostnames enabled.
- **Two Private Subnets** deployed across two distinct Availability Zones for high availability.
- **Dedicated Security Group** restricting inbound database traffic (Port 3306) to internal VPC networks.
- **DB Subnet Group** binding the isolated subnets to the RDS instance.
- **AWS RDS MySQL Instance** configured in private subnets with automated backups and automated storage scaling.

## 📁 Repository Structure

- `main.tf`: Defines the base network infrastructure (VPC, Private Subnets, and Security Group).
- `rds.tf`: Defines the DB Subnet Group and provisions the MySQL RDS instance.
- `.gitignore`: Ignores sensitive Terraform state files and credentials.

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone [https://github.com/Kawtar-cloud-hub/terraform-aws-rds-mysql.git](https://github.com/Kawtar-cloud-hub/terraform-aws-rds-mysql.git)
   cd terraform-aws-rds-mysql
   terraform init
   terraform plan
   terraform apply
