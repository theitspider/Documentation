# Creating a File Share on Windows Server

## Description

This guide provides detailed instructions for creating a file share on a Windows Server. File sharing enables multiple users and systems to access files and folders over a network, facilitating collaboration and efficient resource management.

## Prerequisites

Before starting, ensure that the Windows Server is properly set up and accessible on the network. Administrative privileges on the server are required. Additionally, the folder to be shared should be created and ready for sharing.

## Accessing Server Manager

To begin, open Server Manager, the primary management tool for Windows Server roles, features, and configuration. Server Manager provides a unified interface for installing, configuring, and managing server resources. Open Server Manager from the Start menu or by pressing `Win + X` and selecting "Server Manager".

## Creating a Shared Folder

In Server Manager, navigate to "File and Storage Services" from the left-hand menu. Click on "Shares" to open the file sharing management interface. From here, initiate the New Share Wizard by clicking on "Tasks" and selecting "New Share". The wizard will guide through the process of setting up the file share.


## Selecting the Share Profile

The first step in the New Share Wizard is to select a profile for the share. The "SMB Share - Quick" profile is commonly used for simple file shares. This profile provides basic sharing capabilities suitable for most scenarios. After selecting the profile, proceed by clicking "Next".

## Choosing the Server and Path

Next, select the server and the path of the folder to be shared. This can be done by either browsing for an existing folder or creating a new one. Ensure that the folder is appropriately named and structured for its intended use. Once the folder is selected, click "Next" to move on to the next step.

## Configuring Share Settings

In this step, enter a name for the share. This is the name that users will see when accessing the share over the network. Additional settings can be configured as needed, such as enabling access-based enumeration, which hides files and folders that users do not have permission to access. After configuring these settings, click "Next" to proceed.

![Sharing](<Creating a File Share on Windows Server/Creating a File Share on Windows Server - Sharing.PNG>)

## Specifying Permissions

Configuring permissions for the share is a critical step. Both share permissions and NTFS permissions need to be set to control who can access and modify the shared folder. Add the necessary user groups and set their permissions to either Full Control, Change, or Read, depending on the level of access required. Once the permissions are configured, click "Next" to continue.

![Network Access](<Creating a File Share on Windows Server/Creating a File Share on Windows Server - Network Access.PNG>)

## Completing the Process

Finally, review the configuration settings in the confirmation screen. Ensure that all settings are correct, and then click "Create" to complete the process. After the share is created, click "Close" to exit the wizard. The shared folder is now accessible to users on the network according to the configured permissions.

![Results](<Creating a File Share on Windows Server/Creating a File Share on Windows Server - Results.PNG>)

## Main Points

Creating a file share on a Windows Server is a clear-cut procedure when following these steps. Verify that the server is correctly configured and accessible on the network, with necessary administrative privileges. Once finalized, the shared folder facilitates access for multiple users and systems, promoting collaborative work and efficient resource management.
