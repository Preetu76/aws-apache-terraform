# AWS Apache Web Server – Terraform Project

This project provisions a publicly accessible Apache web server on AWS using Terraform. It sets up the full infrastructure stack required to deploy an EC2 instance with Apache installed and accessible over the internet.

## 🏗️ Architecture Overview

The infrastructure includes the following AWS resources:
- VPC (Virtual Private Cloud)
- Public Subnet
- Internet Gateway
- Route Table and Route Association
- Security Group with HTTP (80) and SSH (22) access
- Elastic IP (EIP)
- Network Interface (ENI)
- EC2 Instance with user_data for Apache setup

## 🚀 Getting Started

### Prerequisites
- [Terraform](https://www.terraform.io/downloads.html) installed
- AWS CLI configured with appropriate IAM permissions
- A key pair in your AWS region for SSH access to EC2

### Setup Instructions

1. **Clone the repository:**

   ```bash
   git clone https://github.com/Preetu76/aws-apache-terraform.git
   cd aws-apache-terraform


### 📋 Prerequisites
- Terraform >= 1.0
- AWS CLI configured with appropriate credentials
- An existing EC2 Key Pair in your AWS account
- Git (optional, for cloning the repo)

### ⚙️ Usage

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Preetu76/aws-apache-terraform.git
   cd aws-apache-terraform
   ```

2. **Initialize the Terraform working directory:**
   ```bash
   terraform init
   ```

3. **Preview the resources Terraform will create:**
   ```bash
   terraform plan
   ```

4. **Apply the configuration:**
   ```bash
   terraform apply
   ```

5. **Access your web server:**
   - Once deployed, Terraform will output the public IP address.
   - Open a browser and visit `http://<public_ip>` to view the Apache test page.

### 🔐 Input Variables (`terraform.tfvars`)

Example:
```hcl
instance_type = "t2.micro"
key_name      = "your-ec2-keypair"
```

> ⚠️ Do **not** commit your `terraform.tfvars` file to GitHub. It may contain sensitive data.

## 🛡️ Security Considerations

- Restrict SSH (port 22) access to your IP instead of `0.0.0.0/0`.
- Never store AWS credentials or `.pem` files in this repository.
- Use IAM roles or environment variables for authentication in production environments.

## 📂 File Structure

```
.
├── main.tf              # Terraform configuration file
├── terraform.tfvars     # Variables file (excluded via .gitignore)
├── .gitignore           # Ignore Terraform state and secrets
├── README.md            # Project documentation
└── LICENSE              # Open source license
```

## 📝 License

This project is licensed under the [MIT License](LICENSE).
=======
# aws-apache-terraform
Provisioning a publicly accessible EC2-based Apache web server on AWS using Terraform, including VPC, subnet, Internet Gateway, route table, security groups, ENI, and Elastic IP configuration.
>>>>>>> 4526dd6919235e87164a5bc385b2a1ea7b2bb941
