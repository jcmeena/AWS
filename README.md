# AWS Infrastructure with Terraform

This repository contains a modular and production-ready **Terraform** architecture to deploy highly secure, scalable, and isolated workloads on **Amazon Web Services (AWS)**. 

Each repo contains a standalone, fully reusable Terraform module tailored for specific infrastructure paradigms.

---

## 🛠️ Project Portfolio

### 1. [Secure SSH Gateway](https://github.com/jcmeena/secure_ssh_to_server) 

### 2. [Multi-Environment Architecture](https://github.com/jcmeena/multi-env)
Demonstrates structural environment separation using explicit directory structures, ensuring parity and parameterization.
* **Isolation Strategy:** Separate state configurations and variables for `dev`, `staging`, and `prod`.
* **DRY Approach:** Utilizes relative modules to minimize boilerplate code across lifecycles.

### 3. [High-Availability Servers behind ALB](https://github.com/jcmeena/webservers_behind_alb)
Features a robust HTTP/HTTPS public ingress layer handling intelligent traffic distribution.
* **Application Load Balancer (ALB):** Public-facing ALB deployed across public subnets with health checks.
* **Target Groups:** Internal routing mechanisms connecting to targets over custom private application ports.

### 4. [Automated Scale-Out Infrastructure](https://github.com/jcmeena/autoscaling_web_servers)
Deploys horizontal elasticity based on resource tracking and real-time metric thresholds.
* **Launch Templates:** Standardized application baselines configuring AMIs, user-data startup scripts, and instance types.
* **Auto Scaling Groups (ASG):** Dynamic rules adjusting min, max, and desired capacity.

### 5. [Managed Kubernetes Service](https://github.com/jcmeena/managed_eks)
Deploys a robust container orchestration engine via **Amazon EKS (Elastic Kubernetes Service)**.

### 6.[Serverless API](https://github.com/jcmeena/serverless_rest_api)
Deploys a lambda function to serve as a REST API
---


## 🚀 Getting Started

### Prerequisites
* [Terraform](https://developer.hashicorp.com/terraform/downloads) (v1.5.0+)
* [AWS CLI v2](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) configured with appropriate IAM administrative privileges.

### Deployment Flow
1. **Clone the repository:**
   ```bash
   git clone <click on the each projects to find out the repo name>
   cd YOUR_REPO_NAME
   ```

2. **Initialize the working workspace (downloads providers & modules):**
   ```bash
   terraform init
   ```
3. **Inspect the architectural execution blueprint:**
   ```bash
   terraform plan
   ```
4. **Provision the live AWS infrastructure resources:**
   ```bash
   terraform apply
   ```

---

## 🧼 Teardown

To avoid unnecessary costs, clean up all generated resources when you are finished by executing:
```bash
terraform destroy
```
