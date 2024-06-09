# Installing OpenSSH with PowerShell

## Description

This guide provides step-by-step instructions for installing OpenSSH on a Windows system using PowerShell. OpenSSH is a suite of secure networking utilities based on the SSH (Secure Shell) protocol, allowing secure remote access and file transfer between computers.

## Prerequisite Check

Ensure that the system is running Windows 10 version 1809 (October 2018 Update) or later, as OpenSSH is included as a feature in these versions of Windows.

## Administrative Access to PowerShell

Right-click on the Start menu and select "Windows PowerShell (Admin)" to open PowerShell with administrative privileges. This is necessary for executing the installation commands.

## Checking OpenSSH Availability

To check if OpenSSH is available, run the following cmdlet:

```powershell
Get-WindowsCapability -Online | Where-Object Name -like 'OpenSSH*'
```

## Install the OpenSSH Client

To install the OpenSSH client, run:

```powershell
Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0
```

## Install the OpenSSH Server

To install the OpenSSH server, run:

```powershell
Add-WindowsCapability -Online -Name OpenSSH.Server~~~~0.0.1.0
```

## Start the sshd Service

To start the sshd service, run:

```powershell
Start-Service sshd
```

## Optional: Set sshd Service to Start Automatically

It is recommended to set the sshd service to start automatically. Run:

```powershell
Set-Service -Name sshd -StartupType 'Automatic'
```

## Confirm Firewall Rule Configuration

To confirm that the Firewall rule is configured correctly, run the following:

```powershell
if (!(Get-NetFirewallRule -Name "OpenSSH-Server-In-TCP" -ErrorAction SilentlyContinue | Select-Object Name, Enabled)) { 
    Write-Output "Firewall Rule 'OpenSSH-Server-In-TCP' does not exist, creating it..." 
    New-NetFirewallRule -Name 'OpenSSH-Server-In-TCP' -DisplayName 'OpenSSH Server (sshd)' -Enabled True -Direction Inbound -Protocol TCP -Action Allow -LocalPort 22 
} else { 
    Write-Output "Firewall rule 'OpenSSH-Server-In-TCP' has been created and exists." 
}
```

## Conclusion

With OpenSSH successfully installed and configured, secure remote access and file transfer between computers are facilitated. This enhances remote administration and communication between devices in a networked environment.