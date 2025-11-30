# Azure Firewall Deployment with Terraform

This project provisions a secure network perimeter in Microsoft Azure using Terraform.  
It was built as part of my learning around cloud networking, Infrastructure as Code (IaC), and modern perimeter security practices.

## What This Deployment Creates

Using the `azurerm` Terraform provider, this setup deploys:

- **Resource Group** – `rg-lbg-demo`
- **Virtual Network** – `lbg-vnet` (`10.0.0.0/16`)
- **Subnet** – `AzureFirewallSubnet` (`10.0.1.0/24`)
- **Public IP Address** – Standard, static
- **Azure Firewall** – Standard tier, deployed into the firewall subnet

This follows Microsoft’s recommended Azure Firewall architecture, with a dedicated subnet and attached public IP.

## Tools & Technologies

- Terraform (HashiCorp)
- Azure CLI
- Azure for Students subscription
- Region used: **Sweden Central** (due to subscription policy restrictions)

## What I Learned

- Writing and applying Infrastructure as Code using Terraform  
- Deploying Azure networking components (VNets, subnets, public IPs, firewalls)  
- Handling Azure policy restrictions and region limitations  
- Troubleshooting real deployment issues (403 forbidden, SKU requirements, etc.)  
- Understanding Azure Firewall and network perimeter security basics

## Screenshots

### Azure Resources Deployed
![Azure Resources](screenshots/resources.png)

### Azure Firewall Overview
![Azure Firewall](screenshots/firewall.png)
