# Adding Roles and Features on Windows Server

## Description

This guide provides step-by-step instructions for adding roles and features on a Windows Server. Roles and features extend the functionality of the server and enable it to perform specific tasks such as domain control, DHCP (Dynamic Host Configuration Protocol), DNS (Domain Name System), and Group Policy management.

## Accessing Server Manager

To begin, access Server Manager, the management tool for Windows Server roles, features, and configuration. Server Manager provides a unified interface for installing, configuring, and managing server roles and features.

![Server Manager](<Adding Roles and Features on Windows Server/Adding Roles and Features on Windows Server - Server Manager.PNG>)

## Adding Roles and Features

### Accessing the Add Roles and Features Wizard

To start, open Server Manager by clicking on its icon on the taskbar or from the start menu. In Server Manager, navigate to the "Manage" menu in the upper right-hand corner and select "Add Roles and Features." This action opens the Add Roles and Features Wizard.

### Before You Begin

On the initial "Before You Begin" page of the wizard, introductory information and prerequisites for adding roles and features are displayed. Read this information carefully to ensure the server meets all requirements, then click "Next" to proceed.

![Before you begin](<Adding Roles and Features on Windows Server/Adding Roles and Features on Windows Server - Before you begin.PNG>)

### Select Installation Type

In the "Select Installation Type" step, choose the type of installation to perform. For most scenarios, select "Role-based or feature-based installation" to add roles and features to a single server or a virtual hard disk. After making this selection, click "Next."

![Installation Type](<Adding Roles and Features on Windows Server/Adding Roles and Features on Windows Server - Installation Type.PNG>)

### Select Destination Server

The next step is the "Select Destination Server" page. Choose the server on which to install the roles and features. The server must be part of the server pool in Server Manager. Select the appropriate server from the list and click "Next" to continue.

![Destination Server](<Adding Roles and Features on Windows Server/Adding Roles and Features on Windows Server - Select Server.PNG>)

### Select Server Roles

On the "Select Server Roles" page, a list of available roles is displayed. This is where the roles to install on the server are chosen. When a role is selected, additional features required for that role may be automatically selected.

![Server Role](<Adding Roles and Features on Windows Server/Adding Roles and Features on Windows Server - Server Role.PNG>)

#### Active Directory Domain Services (ADDS)

To add the Active Directory Domain Services (ADDS) role, check the box next to "Active Directory Domain Services." A new window will appear, listing additional features required for ADDS. Click "Add Features" to include these necessary components. After that, click "Next" to proceed through the wizard.

![Active Directory Domain Services](<Adding Roles and Features on Windows Server/Adding Roles and Features on Windows Server - AD DS.PNG>)

#### DHCP (Dynamic Host Configuration Protocol)

To add the DHCP Server role, check the box next to "DHCP Server." A window will pop up with the features required for DHCP. Click "Add Features" to install these components. Click "Next" to proceed through the wizard.

![Dynamic Host Configuration Protocol](<Adding Roles and Features on Windows Server/Adding Roles and Features on Windows Server - DHCP Server.PNG>)

#### DNS (Domain Name System)

To add the DNS Server role, check the box next to "DNS Server." A pop-up window will display the necessary features for DNS. Click "Add Features" to include them. Click "Next" to proceed through the wizard.

![Domain Name System](<Adding Roles and Features on Windows Server/Adding Roles and Features on Windows Server - DNS Server.PNG>)

### Select Features

#### Group Policy Management

To add the Group Policy Management feature, navigate to the "Select Features" page within the wizard and check the box next to "Group Policy Management." Click "Next" to proceed through the wizard.

### Confirm Installation Selections

After selecting the desired roles and features, the "Confirm Installation Selections" page appears. Review all the selected roles, features, and installation options. Ensure everything is correct before proceeding. If any changes are needed, use the "Previous" button to go back and make adjustments. Once everything is verified, click "Install" to begin the installation process.

![Confirmation](<Adding Roles and Features on Windows Server/Adding Roles and Features on Windows Server - Confirmation.PNG>)

### Installation Progress

During the installation, the "Installation Progress" page displays the status of the installation process. This page shows the progress of each role and feature being installed. Wait for the installation to complete. This process may take some time depending on the number and size of the roles and features being installed.

![Installation Progress](<Adding Roles and Features on Windows Server/Adding Roles and Features on Windows Server - Installation Progress.PNG>)

### Installation Results

Upon completion, the "Installation Results" page will show whether the installation was successful or if any issues occurred. Review the results and ensure all roles and features have been installed correctly. If any errors are present, additional troubleshooting may be required. Once reviewed, click "Close" to exit the wizard.

## Summary

Following these steps, adding roles and features such as Active Directory Domain Services, DHCP, DNS, and Group Policy Management on Windows Server becomes straightforward. These components are essential for managing and controlling network resources, ensuring efficient operation and administration of the server environment.