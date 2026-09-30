# Creating a Resource Group and a Storage Account on Azure for Beginners

**Original publication:** https://dev.to/ifeoma_nwafor/creating-a-resource-group-and-a-storage-account-on-azure-for-beginners-1gkf

**Tags:** #webdev #cloud #azure #cybersecurity

## What is a Resource Group?

A Resource Group in Microsoft Azure is a container that holds related resources for an Azure solution. These resources could include virtual machines, storage accounts, databases, web apps, and more.

## Uses of a Resource Groups

### 1. Organizing Azure Resources

Resource groups help you logically group related Azure resources (like VMs, storage accounts, databases) so they’re easier to manage based on project, environment (dev/test/prod), department, or application.

### 2. Simplified Resource Management

You can manage and monitor all resources in a resource group collectively:

- Deploy or delete resources together
- Apply tags for cost tracking or resource categorization
- Use Azure Policy to enforce rules on all resources in the group

### 3. Access Control and Security

Resource groups support Role-Based Access Control (RBAC):

- Grant specific users or groups permission to only one resource group instead of the whole subscription
- Example: Give a developer team access only to their project’s resource group

### 4. Cost Tracking and Budgeting

By grouping resources by project, team, or department, you can:

- Track costs more easily
- Assign budgets or spending alerts
- Use tags to identify resource ownership and purpose

### 5. Automation and Deployment

You can use tools like:

- ARM templates
- Bicep
- Terraform

to deploy multiple resources to a resource group at once. This ensures consistent, repeatable infrastructure deployments.

### 6. Resource Lifecycle Management

Deleting a resource group deletes all resources inside it. This is useful for:

- Cleaning up after temporary environments (e.g., dev/test)
- Avoiding “resource sprawl” or leftover orphaned services

### 7. Monitoring and Alerts

You can apply:

- Alerts
- Diagnostics settings
- Log analytics

to all resources within a group for centralized monitoring.

## What is a Storage Account?

This is the actual Azure service used to store data. A Storage Account is a top-level container that provides:

- Blobs (object storage)
- Files (file shares)
- Queues (messaging)
- Tables (NoSQL storage)
- Disks (for VMs)

Example: `mystorageaccount.blob.core.windows.net`

## Simple Steps to Create a Resource Group and a Storage Account on Azure

### STEP 1

- In the Azure portal, search for and select Resource groups. Select Create.
- Give your resource group a name. For example, `storagerg`.
- Select a region. Use this region throughout the project.
- Select **Review and create** to validate the resource group.
- Select Create to deploy the resource group.

### STEP 2

Create and deploy a storage account to support testing and training.

- In the Azure portal, search for and select Storage accounts. Select + Create.
- On the Basics tab, select your Resource group.
- Provide a Storage account name. The storage account name must be unique in Azure.
- Set the Performance to Standard.
- Select Review, and then Create.
- Wait for the storage account to deploy and then Go to resource.
