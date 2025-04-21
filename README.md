
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com) [ Coming Soon! ]

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

### Step 1: Provision Azure Virtual Machines

- Deploy two virtual machines:
  - **1 Windows Server 2022 VM** for Active Directory Domain Services
  - **1 Windows 10 VM** as a domain-joined client
- Configure virtual network, subnet, and ensure both VMs are in the same network.

### Step 2: Configure Windows Server and Install AD DS

- Assign a static private IP to the Server VM.
- Rename the server and install the **Active Directory Domain Services** role.
- Promote the server to a **Domain Controller** and create a new forest/domain.

### Step 3: Set Up DNS and Join Client to Domain

- Configure the Windows 10 VM to use the Server VM as its DNS server.
- Join the Windows 10 VM to the newly created domain.
- Restart and verify successful domain join.

### Step 4: Verify and Test Domain Services

- Log in to the Windows 10 VM using domain credentials.
- Use tools like **Active Directory Users and Computers (ADUC)** to create and manage user accounts.
- Optionally test **Group Policy**, **Remote Access**, and **PowerShell AD Commands**.
