# Azure 

Learning azure as cloud services.

## Common terminologies

* Fault domain - Rack, common power source
* Update domain - group of connected hardware that can undergo update, maintaineance at the same time.
* Availability set - collection of fault domain and update domain in the same zone.
* Availability zone - deploy identical VM into separate availability zones which separates the fault domain and update domain.
* ARM - JSON template that can be used to create resources. 
* Virtual Machine scale set - the scale set is to group vm into one image. it can be loaded up or loaded down. Use load balancer before the scale set.

## Common Concepts

* Networking in Azure & Cloud in General. [Sheet](az-network.md)
* Data/databases in Azure [Sheet](az-data.md)
* Messaging in Azire [Sheet](az-messaging.md)

**Make sure the VM are spread across Fault domain and Update domain.**


## Common Azure CLI commands

|Command | Resource Group |
| ----- | ----- |
| az group | Resource group |
| az vm | VM |
| az storage accounts | az storage account |
| az keyvault | Key vault |
| az webapp | Web applications |
| az sql server | SQL DB |
| az cosmosdb | CosmosDB |


## Specific commands

The list to specific commands.

### AZ Group

| command | example | what it does |
| ----- | ----- | ----- |
| `az group create --location --name [--managed-by] [--tags]` | `az group create -l northeurope -n prashamscli-rg` | Creates a new resource group in the given location |
| `az group delete --name` | - | Delete a resource group.|

### AZ Deployment

| command | example | what it does |
| ----- | ----- | ----- |
|`az deployment group create --resource-group <resource_group> --template-file <template_file> --parameters <parameter_file>`| --- | deploy VM using template and parameter file. 

### AZ Storage Account

|command | example | what it does |
| ---- | ---- | ---- |
|`az storage account create --name <name_account> --location <location> --resource group <resource_group> --sku `| --- | To create a new storage account |

### AZ Functionapp

command | example | what it does |
| ---- | ---- | ---- |
|`az functionapp create --name <name_functionapp> --storage-account <name_storage_account> --consumption-plan-location <location> --resource-group <resource_group> --functions-version <version>` | ----| 

### AZ Resources.

| name | What it does |
| ---- | ----- |
| VM | Virtual Machines |
| App Services | Hosting web apps |
| ACR (Cart Docker) | Cart for hosting docker images |
| AKS (Kubernetes services) | Azure k8 services. |
| Azure Functions | Serverless solution to deploy solutions that dont rely on cloud infrastructure and solutions.|
| Logic Apps | Workflow that integrates with apps |
| ACI | Docker without k8.
| App Service Container | Deploy docker to app service |
| App Service Enviornment ASE | Complete isolation of VMs on Vnet & Subnets.|
| Load Balancer | balances load between Vms. **Good for internal resources.**|
| Application Gateway | To manage web apps just as same as Load Balancer. **Good for external resources..** |
| WAF Web Firewall WAF | Protection against common web app threats. |

