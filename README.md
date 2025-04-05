# terraform-ci-cd
# Lab 10 - Terraform CI/CD

This lab shows how to automate Terraform using GitHub Actions. It creates and destroys an EC2 instance on AWS using a CI/CD pipeline.

---

## What It Does

- **Deploys EC2 instance** when code is pushed to the main branch.
- **Destroys EC2 instance** when workflow is triggered manually.
- Uses **GitHub Actions** for automation and **Terraform** to manage infrastructure.

---

## Files Included

- `main.tf`: Terraform code to create an EC2 instance
- `variables.tf`: Variables used in the script
- `.github/workflows/terraform.yml`: GitHub Actions workflow file

---

## Setup Steps

1. Add AWS secrets in GitHub repository:
   - `AWS_ACCESS_KEY_ID`
   - `AWS_SECRET_ACCESS_KEY`
   - `AWS_SESSION_TOKEN` 

2. Push the code to `main` branch – it will create the EC2 instance automatically.

3. To destroy the instance, go to the **Actions** tab and click **“Run workflow”**.

---

## Tags Used

Each EC2 instance is tagged like this:
```hcl
tags = {
  Name = "8894858_E2_Instance"
}
