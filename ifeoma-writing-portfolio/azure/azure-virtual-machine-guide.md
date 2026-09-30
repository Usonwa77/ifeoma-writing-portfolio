# Provisioning a Virtual Machine in Microsoft Azure: A Practical Guide

**Original publication:** https://dev.to/ifeoma_nwafor/provisioning-a-virtual-machine-in-microsoft-azure-a-practical-guide-13dc

**Tags:** #ai #aws #cloud #azure

A virtual machine (VM) is a software-based emulation of a physical computer that runs an operating system and applications using virtualized hardware resources. Creating a virtual machine on the Microsoft Azure Portal or AWS platform allows users to deploy and manage scalable computing resources without purchasing physical hardware. Some key components of a VM include virtual CPU (vCPU), memory (RAM), virtual storage disks, network interfaces, and a hypervisor that manages resource allocation.

Virtual machines are needed to support flexible development, testing, remote work, and workload isolation while optimizing infrastructure costs. For professionals, VMs provide scalability, disaster recovery options, secure environments, and the ability to deploy applications globally within minutes.

As cloud adoption accelerates, virtual machines will continue evolving with automation, AI-driven optimization, and hybrid cloud integration shaping the future of computing.

## Step 1

- On Azure portal search for Virtual Machines.
- Click on Azure Virtual Machine.
- Select virtual machine hosted by Azure.

## Step 2

Select:

- Subscription
- Create Resource group - name it (its preferred to create a new RG for a new VM to avoid mix-up of old and new data)
- Any region of your choice.
- Configure Virtual Machine details, choose a unique name.
- Security - standard
- Operating system - Windows Server Datacenter 64 Gen 2
- Check the spot discount (optional, this is used to minimize cost.
- Authentication type - password
- Choose a username and password of your choice
- Configure inbound port rules - RDP (for Windows), SSH (for Linux)
- Select port 80
- Accept the license agreement

## Step 3

- Go to Monitoring Tab
- Disable Boot Diagnostics

## Step 4

- Go to Tags Tab
- Choose a name and value of your choice. Tags help to identify data on the VM.
- Go to the Review + create Tab
- When the validation process is complete, select "create" to deploy.
- After a successful deployment click on "Go to resource"
- Click on "connect" to kick start your VM.
- To increase your VM's time out, click on public IP address then increase it to 30.

## To download and run Open RDP file

- Select Native RDP - download the file
- Open RDP file on your computer
- Enter Username + password
- Click connect to access VM
- Click continue.

I selected my region as Turkey hence the Turkish language on my virtual machine.

Your virtual computer is ready to be used; you can access any data stored on the cloud.
