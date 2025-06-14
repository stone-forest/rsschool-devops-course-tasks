# RSSchool DevOps Course — Task 1

This repository contains Terraform configuration and GitHub Actions workflow for Task 1.

## Infrastructure

This project provisions:

- ✅ S3 bucket to store Terraform state
- ✅ IAM role for GitHub Actions
- ✅ OpenID Connect (OIDC) trust policy for GitHub identity federation

## Tools & Setup

- Terraform 1.6+
- AWS CLI (configured via IAM user with MFA)
- Terraform state backend: AWS S3
- GitHub Actions for deployment

## GitHub Actions workflow

The workflow consists of:

- `terraform-check` — code format check using `terraform fmt`
- `terraform-plan` — shows execution plan
- `terraform-apply` — applies changes (on push to default branch)

## Region

All resources are deployed to: `us-east-2`
