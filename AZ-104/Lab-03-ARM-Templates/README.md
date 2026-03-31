# Lab 03 - Manage Azure Resources via ARM Templates

**Exam area:** AZ-104 - Deploy and manage Azure compute resources

## Objectives

- Create an Azure Resource Manager (ARM) template by exporting from the portal
- Edit and redeploy an ARM template with modified parameters
- Deploy a resource using the Azure CLI
- Deploy a resource using Azure PowerShell via Cloud Shell
- Deploy a resource using an Azure Bicep template

## Tasks Completed

### Create an Azure Resource Manager template

Exported an ARM template from an existing Azure resource deployment to capture its infrastructure definition as JSON, enabling repeatable deployments.

![Create an Azure Resource Manager template](<Lab 03 - Create an Azure Resource Manager template.png>)

---

### Edit an ARM template and redeploy

Modified the exported ARM template (updated parameters such as SKU and disk size) and redeployed it to demonstrate infrastructure-as-code iteration.

![Edit an Azure Resource Manager template and then redeploy the template](<Lab 03 - Edit an Azure Resource Manager template and then redeploy the template.png>)

---

### Deploy a template with the CLI

Used the Azure CLI (`az deployment group create`) to deploy an ARM template from the command line, demonstrating scriptable, repeatable deployments.

![Deploy a template with the CLI](<Lab 03 - Deploy a template with the CLI.png>)

---

### Configure the Cloud Shell and deploy a template with PowerShell

Configured Azure Cloud Shell and used PowerShell (`New-AzResourceGroupDeployment`) to deploy an ARM template, demonstrating cross-platform IaC tooling.

![Configure the Cloud Shell and deploy a template with PowerShell](<Lab 03 - Configure the Cloud Shell and deploy a template with PowerShell.png>)

---

### Deploy a resource by using Azure Bicep

Authored and deployed an Azure Bicep template (`azuredeployDisk.bicep`) to provision managed disks, demonstrating Bicep as a more readable alternative to raw ARM JSON. The deployment output confirmed all four disks provisioned successfully in the `Succeeded` state.

![Deploy a resource by using Azure Bicep](<Lab 03 - Deploy a resource by using Azure Bicep.png>)
