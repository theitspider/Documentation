# Automating Virtual Machine Creation with Hyper-V Using PowerShell

## Description

This documentation provides a step-by-step guide for automating the creation of virtual machines (VMs) using Hyper-V and PowerShell scripting. By following these instructions, users can streamline the process of provisioning VMs, saving time and reducing the risk of errors associated with manual configuration. The guide covers essential tasks such as configuring VM settings, attaching ISO images, and starting VMs.

## Installation of Hyper-V and PowerShell Module

Ensure that Hyper-V is installed on the system and the Hyper-V PowerShell module is available. If not installed, enable it through the "Windows Features" menu.

## Preparing the PowerShell Script

Create a new PowerShell script file (.ps1) using any preferred text editor. Start the script by importing the Hyper-V module to gain access to the cmdlets required for VM management.

## Defining VM Configuration

Define the configuration for the new virtual machine, including name, memory, processor count, network settings, etc. Store these configurations in variables for ease of use. If required, create a virtual switch for the VM to connect to the network.

## Creating the Virtual Machine

- Use the **New-VM** cmdlet to create the virtual machine using the configurations defined earlier.
- If installing an operating system, attach the ISO/image to the virtual machine using **Add-VMDvdDrive**.
- Start the newly created virtual machine using the **Start-VM** cmdlet.

## Configuring Optional Settings

Depending on requirements, set additional configurations such as assigning static MAC addresses, configuring checkpoints, etc.

## Verification of Virtual Machine Creation

After running the script, verify that the VM has been created successfully by checking Hyper-V Manager or using PowerShell cmdlets like **Get-VM**.