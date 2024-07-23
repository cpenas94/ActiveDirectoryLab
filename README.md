# Active Directory Lab Setup

## Overview

This repository contains the documentation for setting up and configuring an Active Directory (AD) environment on Windows Server. The setup demonstrates the manual installation and configuration of Active Directory Domain Services (AD DS) and includes information about the setup process and configuration steps.

## Installation

### Prerequisites

- **Oracle VM VirtualBox**: Virtualization software used to create a virtual machine.
- **Windows Server ISO**: The installation media for Windows Server.
- **Windows Server License**: Use the evaluation version if available.

### Steps

1. **Create a Virtual Machine**:
   - Set up a new virtual machine in Oracle VM VirtualBox with the Windows Server ISO attached.

2. **Install Windows Server**:
   - Boot the VM with the installation media and select **Custom** installation for a clean setup.

3. **Configure the Local Server**:
   - Set a static IP address for the server.
   - Rename the server to a meaningful name, such as `ADLabServer`.

4. **Install Active Directory Domain Services (AD DS)**:
   - Open **Server Manager** and navigate to **Add Roles and Features**.
   - Select the **Active Directory Domain Services** role and complete the installation.

5. **Promote the Server to a Domain Controller**:
   - In **Server Manager**, click on the notification flag and select **Promote this server to a domain controller**.
   - Configure the domain settings and promote the server to a domain controller for the domain `adlab.local`.

## Manual Configuration

### Create Organizational Units (OUs)

1. **Open Active Directory Users and Computers**:
   - Navigate to **Server Manager** > **Tools** > **Active Directory Users and Computers**.

2. **Create OUs**:
   - Right-click on the domain (e.g., `adlab.local`), choose **New** > **Organizational Unit**.
   - Create OUs such as `Students`, `Staff`, and `Computers` as needed.

### Create User Accounts

1. **Navigate to the OU**:
   - Select the OU where you want to create user accounts.

2. **Add New Users**:
   - Right-click on the OU, select **New** > **User**.
   - Enter the user's first name, last name, and username. Set a strong password and configure account options.

3. **Repeat**:
   - Continue creating additional user accounts in the appropriate OUs.

## Configuration Files

- **`ad-setup.txt`**: Contains basic information about the Active Directory setup, including domain name, domain controller, and DNS server settings.

## Future Enhancements

- **Automation**: Consider creating PowerShell scripts for bulk user creation and other repetitive tasks to streamline the setup process.
- **Advanced Features**: Explore additional Active Directory features such as Group Policy, advanced security settings, and integration with other services.


## Acknowledgments

- Oracle VM VirtualBox for virtualization.
- Microsoft for providing the Windows Server evaluation version.

