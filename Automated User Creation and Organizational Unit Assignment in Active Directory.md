# Automated User Creation and Organizational Unit Assignment in Active Directory

## Description

This guide presents a PowerShell script for automating the creation of user accounts in Active Directory (AD) and assigning them to specified Organizational Units (OUs).

## Script

```powershell
# Variables necessary for account creation
$FirstName = Read-Host -Prompt "Enter first name"
$LastName = Read-Host -Prompt "Enter last name"
$UserName = Read-Host -Prompt "Enter username"
$Password = Read-Host -Prompt "Enter a password (minimum 8 characters)"

# AD account creation
New-ADUser `
-Name $UserName `
-Surname $LastName `
-GivenName $FirstName `
-UserPrincipalName $UserName `
-AccountPassword (ConvertTo-SecureString $Password -AsPlainText -Force) `
-Path "OU=Test,DC=puteaux,DC=local"

# Enabling and displaying the AD account
Enable-ADAccount -Identity $UserName
Get-ADUser -Identity $UserName
```

## Explanation

The script prompts for user details including first name, last name, username, and password (minimum 8 characters) required for creating a user account in Active Directory. It then utilizes the `New-ADUser` cmdlet to create the new user account, setting attributes such as name, surname, given name, user principal name, account password, and OU path. The OU path specifies the location where the user account will be created within the Active Directory structure.

After creating the user account, the script enables the account using the `Enable-ADAccount` cmdlet to ensure the account is active for authentication purposes. Finally, it retrieves and displays the details of the newly created user account using the `Get-ADUser` cmdlet, providing confirmation of the successful creation of the user account.

## Usage Instructions

To utilize this script, follow these steps: Open PowerShell. Ensure that the Active Directory module is imported into the PowerShell session using `Import-Module ActiveDirectory`. Copy and paste the script into the PowerShell window. Follow the prompts to input the required user details: first name, last name, username, and password. The script will create the user account in the specified OU, enable it, and display the user details.

![Example](<Automated User Creation and Organizational Unit Assignment in Active Directory/Automated User Creation and Organizational Unit Assignment in Active Directory - Example.PNG>)<br>
![Results](<Automated User Creation and Organizational Unit Assignment in Active Directory/Automated User Creation and Organizational Unit Assignment in Active Directory - Results.PNG>)

## Notes

Ensure that the password meets the organization's complexity requirements. Modify the `-Path` parameter in the script to match the desired Organizational Unit (OU) in the Active Directory structure. Additional parameters can be added to the `New-ADUser` cmdlet to set more attributes for the user account as needed.

## Conclusion

This script streamlines the process of creating user accounts in Active Directory and assigning them to specific Organizational Units, reducing manual effort and ensuring consistency in user management procedures. By automating these tasks, administrators can efficiently manage user accounts, enhancing the overall security and organization of their Active Directory environment.