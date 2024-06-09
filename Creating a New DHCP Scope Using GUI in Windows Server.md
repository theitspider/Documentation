# Creating a New DHCP Scope Using GUI in Windows Server

## Description

This comprehensive guide walks through the process of creating a new DHCP scope using the graphical user interface (GUI) in Windows Server.

## Prerequisites

Before proceeding, ensure the server is running Windows Server, has a static IP address, and is connected to the network. Install the DHCP Server role, update the server, and have administrative credentials ready. Determine the IP address range and subnet mask for the new DHCP scope before starting the configuration process.

## Open DHCP Manager

To begin creating a new DHCP scope, launch Server Manager by clicking on the Start menu and selecting "Server Manager" from the list of applications. In Server Manager, click on "Tools" in the top right corner and select "DHCP" from the drop-down menu to open the DHCP Manager.

## Create a New Scope

In the DHCP Manager, expand the server node where the DHCP role is installed. Right-click on "IPv4" and select "New Scope" to open the New Scope Wizard. This wizard will guide through the process of setting up the new scope.

![New Scope](<Creating a New DHCP Scope Using GUI in Windows Server/Creating a New DHCP Scope Using GUI in Windows Server - New Scope.PNG>)

## Scope Name and Description

In the New Scope Wizard, click "Next" on the welcome page. Enter a name and description for the new DHCP scope to help identify it later. Click "Next" to continue.

![Scope Name](<Creating a New DHCP Scope Using GUI in Windows Server/Creating a New DHCP Scope Using GUI in Windows Server - Scope Name.PNG>)

## IP Address Range

Specify the IP address range for the scope by entering the start and end IP addresses. Additionally, enter the subnet mask for the IP address range. These settings define the pool of IP addresses that the DHCP server will manage and distribute. Click "Next" to proceed.

![IP Address Range](<Creating a New DHCP Scope Using GUI in Windows Server/Creating a New DHCP Scope Using GUI in Windows Server - IP Address Range.PNG>)

## Add Exclusions and Delay

Add any IP address exclusions by specifying the start and end IP addresses to be excluded from the DHCP scope. This is useful for reserving addresses for static IP devices. Click "Add" for each exclusion, and set the delay in milliseconds if required. Click "Next" to continue.

![Add Exclusions and Delay](<Creating a New DHCP Scope Using GUI in Windows Server/Creating a New DHCP Scope Using GUI in Windows Server - Add Exclusions and Delay.PNG>)

## Lease Duration

Set the lease duration, which determines how long a client can use an IP address assigned by the DHCP server. The default duration is 8 days, but it can be adjusted based on network needs. Click "Next" to proceed.

![Lease Duration](<Creating a New DHCP Scope Using GUI in Windows Server/Creating a New DHCP Scope Using GUI in Windows Server - Lease Duration.PNG>)

## Configure DHCP Options

Choose whether to configure DHCP options now or later. Select "Yes, I want to configure these options now" and click "Next." This choice allows setting up essential network options immediately.

![Configure DHCP Options](<Creating a New DHCP Scope Using GUI in Windows Server/Creating a New DHCP Scope Using GUI in Windows Server - Configure DHCP Options.PNG>)

## Router (Default Gateway)

Enter the IP address of the router (default gateway) for the network. This is the address that clients will use to access devices outside their subnet. Click "Add" to include it in the list, then click "Next" to proceed.

![Router (Default Gateway)](<Creating a New DHCP Scope Using GUI in Windows Server/Creating a New DHCP Scope Using GUI in Windows Server - Router (Default Gateway).PNG>)

## Domain Name and DNS Servers

Enter the parent domain name and the IP addresses of the DNS servers for the network. These settings help clients resolve domain names to IP addresses. Click "Add" for each DNS server, then click "Next" to continue.

![Domain Name and DNS Servers](<Creating a New DHCP Scope Using GUI in Windows Server/Creating a New DHCP Scope Using GUI in Windows Server - Domain Name and DNS Servers.PNG>)

## WINS Servers

If using WINS servers, enter their IP addresses and click "Add" for each WINS server. This step is optional and specific to environments using WINS for name resolution. Click "Next" to proceed.

![WINS Servers](<Creating a New DHCP Scope Using GUI in Windows Server/Creating a New DHCP Scope Using GUI in Windows Server - WINS Servers.PNG>)

## Activate Scope

Choose whether to activate the scope now or later. Select "Yes, I want to activate this scope now" to start using the scope immediately, then click "Next."

![Activate Scope](<Creating a New DHCP Scope Using GUI in Windows Server/Creating a New DHCP Scope Using GUI in Windows Server - Activate Scope.PNG>)

## Complete the Wizard

Review the configuration summary and ensure all settings are correct. Click "Finish" to complete the New Scope Wizard and finalize the creation of the DHCP scope.

![Completing the New Scope Wizard](<Creating a New DHCP Scope Using GUI in Windows Server/Creating a New DHCP Scope Using GUI in Windows Server - Completing the New Scope Wizard.PNG>)

## Summary

Creating a new DHCP scope via the GUI in Windows Server provides a straightforward approach to managing IP address distribution within a network. Following these steps ensures an efficient configuration process, enabling dynamic IP address allocation and network management.