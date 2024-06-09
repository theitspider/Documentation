# Installing Hyper-V on a Machine

## Description

This guide outlines Hyper-V installation on a machine via PowerShell commands. Hyper-V, a hypervisor-based virtualization tool for Windows, facilitates VM creation and management. The steps ensure swift setup for testing, development, and production needs. It covers prerequisites, feature activation, and verification.

## Prerequisite Check

Ensure that the system meets the prerequisites for installing Hyper-V. This includes having a 64-bit version of Windows 10 or Windows Server, a compatible processor with virtualization support, and hardware-assisted virtualization enabled in the BIOS settings.

## Administrative Access to PowerShell

Right-click on the Start menu and select "Windows PowerShell (Admin)" to open PowerShell with administrative privileges. This is necessary for executing the installation commands.

## Enabling Hyper-V Features

Execute the PowerShell command provided below to activate Hyper-V features:

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All
```

![Enabling Hyper-V Features](<Installing Hyper-V on a Machine/Installing Hyper-V on a Machine - Enabling Hyper-V Features.PNG>)<br>
![Enable Hyper-V with CMD and DISM](<Installing Hyper-V on a Machine/Installing Hyper-V on a Machine - Enable Hyper-V with CMD and DISM.PNG>)

This command triggers the activation of all essential Hyper-V components on the system, initiating the installation process.

## System Restart

After enabling Hyper-V features, restart the system to apply the changes. This step is essential to complete the installation process.

## Verification of Hyper-V Installation

Once the system has restarted, open PowerShell as Administrator again and execute the following command to verify that Hyper-V is installed and running:

```powershell
Get-WindowsFeature -Name Hyper-V | Select-Object -Property Name,Installed
```
![Hyper-V Manager](<Installing Hyper-V on a Machine/Installing Hyper-V on a Machine - Hyper-V Manager.PNG>)

## Additional Configuration (Optional)

Depending on requirements, perform additional configuration steps such as configuring virtual switches, setting up networking, or adjusting Hyper-V settings. These configurations can be done using PowerShell cmdlets or through the Hyper-V Manager graphical interface.

## Starting Virtual Machine Creation

With Hyper-V successfully installed and verified, virtual machines can be promptly created and managed on the system. Whether utilizing the Hyper-V Manager or PowerShell cmdlets, virtualization technology can be harnessed for various purposes, including testing, development, or production environments.