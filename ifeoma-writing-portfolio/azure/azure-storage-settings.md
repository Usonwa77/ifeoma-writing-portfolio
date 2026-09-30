# How to Configure Simple Settings in the Storage Account on Azure

**Original publication:** https://dev.to/ifeoma_nwafor/how-to-configure-simple-settings-in-the-storage-account-on-azure-14bm

**Tags:** #webdev #learning #beginners #azure

Simple steps on how to configure simple settings in the storage account on Azure.

## STEP 1

When the data in this storage account doesn’t require high availability or durability and a lowest cost storage solution is desired:

- In your storage account, in the Data management section, select the Redundancy blade.
- Select Locally-redundant storage (LRS) in the Redundancy drop-down. Be sure to Save your changes.
- Refresh the page and notice the content only exists in the primary location.

## STEP 2

When the storage account should only accept requests from secure connections and developers would like the storage account to use at least TLS version 1.2:

- In the Settings section, select the Configuration blade.
- Ensure Minimal TLS version is set to Version 1.2.
- Ensure Allow storage account key access is Disabled.
- Be sure to Save your changes.

## STEP 3

To ensure the storage account allows public access from all networks:

- In the Security + networking section, select the Networking blade.
- Ensure Public network access is set to Enabled from all networks.
- Be sure to Save your changes.
