# Creating a Group Policy Object (GPO) on Windows Server

## Description

This guide provides detailed instructions for creating a Group Policy Object (GPO) on a Windows Server. GPOs are vital for managing and configuring operating systems, applications, and user settings within an Active Directory environment. They allow administrators to enforce specific configurations and security settings across the network, ensuring consistency and compliance.

## Accessing Group Policy Management Console (GPMC)

To begin creating a GPO, access the Group Policy Management Console (GPMC), which is the tool used for creating, editing, and managing GPOs. Start by logging into the Windows Server with an account that has administrative privileges. Open Server Manager from the Start menu. In Server Manager, click on "Tools" and select "Group Policy Management" from the dropdown menu to open the GPMC.

![Group Policy Management](<Creating a Group Policy Object (GPO) on Windows Server/Creating a Group Policy Object (GPO) on Windows Server - Group Policy Management.PNG>)

## Creating and Linking a New GPO

Within the GPMC, navigate to the domain or organizational unit (OU) where the new GPO will be created. Right-click the domain or OU, and select "Create a GPO in this domain, and Link it here...". In the dialog box that appears, enter a name for the GPO. Optionally, provide a description to explain the purpose of the GPO. After naming the GPO, click "OK" to create and link it to the selected domain or OU.

![New GPO Name](<Creating a Group Policy Object (GPO) on Windows Server/Creating a Group Policy Object (GPO) on Windows Server - New GPO Name.PNG>)

## Editing the GPO

Once the GPO is created, it needs to be configured to enforce specific policies. Right-click the newly created GPO and select "Edit" to open the Group Policy Management Editor. This editor allows configuring policies under both Computer Configuration and User Configuration sections. Each section has subcategories for Policies and Preferences, where various configurations can be set. For example, to set a policy for password complexity, navigate to Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy. Double-click "Password must meet complexity requirements," enable the setting, and apply the changes.

![Group Policy Management Editor](<Creating a Group Policy Object (GPO) on Windows Server/Creating a Group Policy Object (GPO) on Windows Server - Group Policy Management Editor.PNG>)

## Linking the GPO to Additional OUs

If the GPO needs to apply to other OUs, it can be linked accordingly. In the GPMC, right-click the additional OU where the GPO should apply, and select "Link an Existing GPO...". Choose the GPO created from the list and click "OK" to link it to the selected OU.

![Linking an existing GPO to a Domain](<Creating a Group Policy Object (GPO) on Windows Server/Creating a Group Policy Object (GPO) on Windows Server - Linking an existing GPO to a Domain.PNG>)

## Applying the GPO

To ensure the GPO settings take effect immediately, refresh Group Policy on the client computers. Open Command Prompt on the client computer and type `gpupdate /force`, then press Enter. This command forces a refresh of Group Policy settings, applying the new configurations set in the GPO.

## Summary

Creating and configuring Group Policy Objects (GPOs) on Windows Server involves accessing the Group Policy Management Console, creating and linking a new GPO, editing the GPO to set specific policies, optionally linking it to additional OUs, and ensuring the policies are applied by refreshing Group Policy. These steps allow administrators to efficiently manage and enforce settings across an Active Directory environment, ensuring consistent configurations and compliance with organizational policies.