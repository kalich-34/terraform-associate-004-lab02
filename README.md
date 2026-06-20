# terraform-associate-004-lab02

## Lab Overview
This Terraform lab creates a single AWS VPC in the `us-east-1` region using the AWS provider.

## Files
- `providers.tf`: configures the AWS provider and required provider version.
- `main.tf`: defines an `aws_vpc` resource with `10.0.0.0/16` CIDR.
- `.gitignore`: ignores local Terraform state, CLI files, and `.terraform` directories.
- `.terraform.lock.hcl`: locks provider dependency versions.

## Prerequisites
- AWS CLI configured with valid AWS credentials.
- Terraform installed locally.
- Access to AWS account resources in `us-east-1`.

## Terraform Commands
1. Initialize the working directory:
   ```bash
   terraform init
   ```
2. Preview the planned changes:
   ```bash
   terraform plan
   ```
3. Apply the configuration:
   ```bash
   terraform apply
   ```
   Confirm with `yes` when prompted.

## Resource Created
- `aws_vpc.main`: an Amazon VPC with CIDR block `10.0.0.0/16`.

## Cleanup
To remove the AWS resources created by this lab, run:
```bash
terraform destroy
```

## Notes
- Do not check in `terraform.tfstate` or `terraform.tfstate.backup`.
- Commit `.terraform.lock.hcl` if you want to preserve provider version locking.
