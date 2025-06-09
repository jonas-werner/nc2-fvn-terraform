# Nutanix Cloud Clusters (NC2) Flow Virtual Networking (FVN) Terraform Samples

This repository contains a collection of Terraform samples demonstrating different Flow Networking configurations in Nutanix Cloud Infrastructure (NCI). These samples show how to set up various networking scenarios using Terraform. Also included are VM image downloads from public repositories and VM creation. 

## Prerequisites

- Nutanix Cloud Infrastructure (NCI) cluster
- Prism Central instance
- Terraform installed (version 1.0.0 or later)
- Nutanix Terraform provider (version 2.2.0 or later)



## Nutanix software versions
These samples have been tested and verified on NC2 on AWS with the following Nutanix software versions. 
- Prism Central: pc.2024.3.1.1
- AOS: 10.0.1
- AHV: 7.0.1.5


## Available Samples

1. **nc2-fvn_nat-vpcs**: Demonstrates how to create NAT-enabled VPCs with multiple subnets
2. **nc2-fvn_nat-vms-simple**: Shows how to deploy VMs in a NAT-enabled VPC environment
3. **nc2-os-images**: Contains examples for managing OS images in NCI
4. **nc2-fvn_nonat-vpcs**: Illustrates the creation of no-NAT VPCs
5. **nc2-fvn_nonat-only**: Shows how to set up a no-NAT only networking environment
6. **nc2-fvn_nat-nonat-vms**: Demonstrates deploying VMs in a mixed NAT/no-NAT environment

## Usage

Each sample directory contains:
- `main.tf`: Main Terraform configuration
- `variables.tf`: Variable definitions
- `terraform.tfvars`: Variable values
- `set-env.sh`: Environment setup script

To use any sample:

1. Navigate to the desired sample directory
2. Source the environment variables:
   ```bash
   source set-env.sh
   ```
3. Initialize Terraform:
   ```bash
   terraform init
   ```
4. Review the planned changes:
   ```bash
   terraform plan
   ```
5. Apply the configuration:
   ```bash
   terraform apply
   ```

## Environment Variables

Each sample requires the following environment variables (set via `set-env.sh`):
- `TF_VAR_NUTANIX_USERNAME`: Prism Central username
- `TF_VAR_NUTANIX_PASSWORD`: Prism Central password
- `TF_VAR_NUTANIX_ENDPOINT`: Prism Central IP/FQDN
- `TF_VAR_NUTANIX_PORT`: Prism Central port (default: 9440)
- `TF_VAR_NUTANIX_INSECURE`: Set to "true" if using self-signed certificates
- `TF_VAR_SSH_PUBLIC_KEY`: SSH public key for VM access

