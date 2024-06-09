# Joining a Windows Computer to a Domain

## Description

This guide provides step-by-step instructions for joining a Windows computer to a domain. Joining a domain allows the computer to access network resources and be managed centrally using Active Directory Domain Services (ADDS). This process is essential for integrating the computer into an organizational network.

## Prerequisites

Before starting, ensure the computer is connected to the network where the domain controller is accessible. The fully qualified domain name (FQDN) of the domain is required, along with a user account that has permissions to join computers to the domain. Additionally, decide on a unique name for the computer within the domain.

## Accessing System Properties

To begin, open the Settings app by pressing `Win + I` and navigate to "System". Scroll down and click on "About", then select "System info" to open the classic System Properties window. In the System Properties window, click on "Change settings" on the right side. This will open the System Properties dialog box, where the "Change..." button should be clicked.

![Rename this PC (advanced)](<Joining a Windows Computer to a Domain/Joining a Windows Computer to a Domain - Rename this PC (advanced).PNG>)

## Changing Computer Name and Domain

In the "Computer Name/Domain Changes" window, select "Domain" under the "Member of" section and enter the domain name to be joined. Click "OK" to proceed. When prompted, enter the domain user name and password with permissions to join the computer to the domain. The computer will contact the domain controller to authenticate and join the domain.

![Change](<Joining a Windows Computer to a Domain/Joining a Windows Computer to a Domain - Change.PNG>)<br>
![Administrator Credentials](<Joining a Windows Computer to a Domain/Joining a Windows Computer to a Domain - Credentials.PNG>)<br>
![Domain Welcome Message](<Joining a Windows Computer to a Domain/Joining a Windows Computer to a Domain - Domain Welcome Message.PNG>)
## Completing the Process

After successfully joining the domain, a prompt to restart the computer will appear. Click "OK" to close the dialog boxes, then restart the computer to apply the changes. After restarting, log in with domain credentials. To verify domain membership, open the System Properties window again and confirm that the domain name is listed.

![Results](<Joining a Windows Computer to a Domain/Joining a Windows Computer to a Domain - Results.PNG>)<br>
![Restart Message](<Joining a Windows Computer to a Domain/Joining a Windows Computer to a Domain - Restart Message.PNG>)

## Troubleshooting Tips

If issues are encountered, ensure the computer can communicate with the domain controller by checking the network connection and DNS settings. Verify that the domain account used has sufficient permissions to join a computer to the domain. Ensure that firewall settings on the computer and the network allow communication with the domain controller. Additionally, make sure the computer's time is synchronized with the domain controller, as time discrepancies can cause authentication issues.

## Wrap-Up

By following these steps, joining a Windows computer to a domain becomes straightforward. Ensure the necessary network connection, domain information, and appropriate permissions are in place. Once the computer is part of the domain, it can access network resources and be managed centrally using Active Directory Domain Services, enhancing the efficiency and security of network administration.