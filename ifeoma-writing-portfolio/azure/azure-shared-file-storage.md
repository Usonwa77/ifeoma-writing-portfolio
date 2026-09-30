# Providing Shared File Storage on Azure

**Original publication:** https://dev.to/ifeoma_nwafor/providing-shared-file-storage-on-azure-2bp5

**Tags:** #beginners #azure #startup #cloud

## How to Provide Shared File Storage

### STEP 1

- In the portal, search for and select **Storage accounts**. Select + Create.
- For Resource group select Create new. Give your resource group a name and select **OK** to save your changes.
- Provide a Storage account name. Ensure the name meets the naming requirements.
- Set the Performance to Premium.
- Set the Premium account type to File shares.
- Set the Redundancy to Zone-redundant storage.
- Select Review and then Create the storage account.
- Wait for the resource to deploy.
- Select Go to resource.

### STEP 2

Create and configure a file share with directory.

Example: Create a file share for the corporate office.

- In the storage account, in the Data storage section, select the File shares blade.
- Select + File share and provide a Name.
- Review the other options, but take the defaults.
- Select Create.

### STEP 3

Configure and test snapshots. Similar to blob storage, you need to protect against accidental deletion of files. You decide to use snapshots.

- Select your file share.
- In the Operations section, select the Snapshots blade.
- Select + Add snapshot. The comment is optional. Select OK.
- Select your snapshot and verify your file directory and uploaded file are included.

### STEP 3a

Configure restricting storage access to selected virtual networks.

This task in this section requires a virtual network with subnet. In a production environment these resources would already be created.

- Search for and select Virtual networks.
- Select Create. Select your resource group and give the virtual network a name.
- Take the defaults for other parameters, select Review + create, and then Create.
- Wait for the resource to deploy.
- Select Go to resource.
- In the Settings section, select the Subnets blade.
- Select the default subnet. In the Service endpoints section choose **Microsoft.Storage** in the Services drop-down.
- Do not make any other changes.
- Be sure to Save your changes.

### STEP 4

The storage account should only be accessed from the virtual network you just created.

- Return to your files storage account.
- In the Security + networking section, select the Networking blade.
- Change the Public network access to Enabled from selected virtual networks and IP addresses.
- In the Virtual networks section, select Add existing virtual network.
- Select your virtual network and subnet, select Add.
- Be sure to Save your changes.
- Select the Storage browser and navigate to your file share.
- Verify the message not authorized to perform this operation. You are not connecting from the virtual network.
