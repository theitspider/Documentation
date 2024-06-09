# Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server

## Description

This comprehensive guide walks through the process of promoting a server to a Domain Controller (DC) using the graphical user interface (GUI) in Windows Server.

## Prerequisites

Before proceeding, ensure the server is running Windows Server, has a static IP address, and is connected to the network. Install Server Manager, update the server, and have administrative credentials ready. Decide on the root domain name for the Active Directory forest before starting the promotion process.

## Promote to Domain Controller

Once the installation of Active Directory Domain Services (AD DS) is completed, a notification will appear at the top of Server Manager, indicating that the AD DS installation is pending. Clicking on it initiates the Active Directory Domain Services Configuration Wizard.

## Deployment Configuration

In the Configuration Wizard, select "Add a new forest" and proceed to enter the root domain name for the Active Directory forest. Click "Next" to continue.

![Deployement Configuration](<Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server/Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server - Deployment Configuration.PNG>)

## Domain Controller Options

Upon entering the domain name, select the appropriate options for the deployment, including Domain Controller options and the Directory Services Restore Mode (DSRM) password. Ensure all necessary configurations are set up before proceeding to the next step.

![Domain Controller Options](<Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server/Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server - Domain Controller Options.PNG>)

## DNS Options

If prompted, select "DNS server" to enable the Domain Name System (DNS) role on the Domain Controller. This step ensures proper domain name resolution within the network environment.

![DNS Options](<Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server/Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server - DNS Options.PNG>)

## Additional Options

Review any additional options presented in the Configuration Wizard and make necessary adjustments according to network requirements. Click "Next" to proceed once all configurations are finalized.

![Additional Options](<Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server/Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server - Additional Options.PNG>)

## Paths

Review the default paths for the database, log files, and SYSVOL folder. Ensure that these paths align with organization's storage and backup policies. Click "Next" to continue.

![Paths](<Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server/Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server - Paths.PNG>)

## Review Options

Before initiating the installation process, carefully review the configuration summary provided by the Configuration Wizard. Verify that all settings are accurate and aligned with network infrastructure requirements.

![Review Options](<Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server/Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server - Review Options.PNG>)<br>
![Prerequisites Check](<Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server/Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server - Prerequisites Check.PNG>)

## Installation Progress

Once satisfied with the configuration settings, proceed to start the installation process. Wait for the installation progress to complete. Depending on the server's specifications, this process may take some time.

![Installation Progress](<Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server/Promoting a Server to a Domain Controller (DC) Using GUI in Windows Server - Installation.PNG>)

## Post-Installation

After the installation process is finished, the server will restart automatically. Upon restart, log in using the Administrator credentials. Active Directory Domain Services will now be installed, and the server will be successfully promoted to a Domain Controller.

## Wraping Up

Promoting a server to a Domain Controller via the GUI in Windows Server offers a user-friendly approach to establishing a domain-based network environment. Following these steps ensures a seamless transition and enables centralized management of users, computers, and resources within the domain.