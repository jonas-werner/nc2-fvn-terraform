# Mixed NAT/Non-NAT VMs Example

This example demonstrates how to deploy virtual machines in a mixed NAT and no-NAT environment using Terraform in Nutanix Cloud Clusters (NC2).

## Overview

This configuration:
- Creates VMs in both NAT and no-NAT VPCs
- Configures networking for different VM types
- Sets up cloud-init for VM initialization

## Prerequisites

- Existing NAT and non-NAT VPCs
- OS image available in Prism Central
- Prism Central access
- SSH public key for VM access
- Understanding of mixed networking requirements

## Usage

1. Set up environment variables:
   ```bash
   source set-env.sh
   ```

2. Initialize Terraform:
   ```bash
   terraform init
   ```

3. Review the planned changes:
   ```bash
   terraform plan
   ```

4. Apply the configuration:
   ```bash
   terraform apply
   ```

## Configuration Details

The configuration:
- Deploys VMs in both NAT and no-NAT environments
- Uses cloud-init for VM initialization
- Configures networking and security for each environment
- Handles mixed networking scenarios

## Templates

The `templates` directory contains:
- Cloud-init configuration templates
- VM initialization scripts
- Network configuration templates for both NAT and no-NAT environments

## Variables

Key variables in `terraform.tfvars`:
- VM names and configurations
- Network settings for both environments
- Resource specifications
- Environment-specific parameters

## Cleanup

To destroy the created resources:
```bash
terraform destroy
``` 