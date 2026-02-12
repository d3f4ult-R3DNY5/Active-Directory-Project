# Basic Scripts using PowerShell

## Overview 
---
This Writeup covers the different ways PowerShell can be used to simplify repetitive administrative tasks. Through scripting and automation, PowerShell allows administrators to efficiently manage user accounts, including the creation, modification, and deletion of users, reducing manual effort and improving consistency.

>[!NOTE]
>- Fetching the User Information
>- Creating the User Account 
>- Scripting Automation for the Disabled Accounts
>- Creating the User accounts from the CSV files and handling the duplicates 

### Scripts
---
#### Fetching the user accounts

- Using the command `Get-ADUser -identity` Command

![](../Attachments/Pasted%20image%2020260211113633.png)

- Using the command `Get-ADUser - Filter {Expressions} `

![](../Attachments/Pasted%20image%2020260211114121.png)

#### Script To fetch the Name belonging To a Particular OU 

![](../Attachments/Pasted%20image%2020260211114921.png)

![](../Attachments/Pasted%20image%2020260211114934.png)

**Exporting them to a CSV**

![](../Attachments/Pasted%20image%2020260211115231.png)

![](../Attachments/Pasted%20image%2020260211115601.png)

#### Getting the members of the group 

![](../Attachments/Pasted%20image%2020260211122928.png)

![](../Attachments/Pasted%20image%2020260211122946.png)

#### Group details 

![](../Attachments/Pasted%20image%2020260211123249.png)

![](../Attachments/Pasted%20image%2020260211123304.png)

#### Adding a user to the to the Sales OU and Marketing Group

![](../Attachments/Pasted%20image%2020260211130059.png)

![](../Attachments/Pasted%20image%2020260211130153.png)

#### Adding the users from the CSV file 

```powershell
Import-Module ActiveDirectory

$Users = Import-Csv (Read-Host "Enter The File Path to be Read")

$CreatedUsernames = [System.Collections.Generic.List[string]]::new()

function Get-UniqueUsername {
    param ([string]$FirstName, [string]$LastName)

    $base     = $FirstName.Substring(0,1).ToUpper() + $LastName
    $username = $base
    $display  = "$FirstName $LastName"
    $counter  = 1

    while ((Get-ADUser -Filter "SamAccountName -eq '$username'" -ErrorAction SilentlyContinue) -or ($script:CreatedUsernames -contains $username)) {
        $username = "$base$counter"
        $display  = "$FirstName $LastName $counter"
        $counter++
    }

    $script:CreatedUsernames.Add($username)
    return @($username, $display)
}

foreach ($user in $Users) {
    $uname = $null
    try {
        $enabled = if ($user.AccountStatus -eq "Enabled") { $true } else { $false }
        $uname, $display = Get-UniqueUsername -FirstName $user.FirstName -LastName $user.LastName

        New-ADUser `
            -Name             $display `
            -GivenName        $user.FirstName `
            -Surname          $user.LastName `
            -Description      $user.Description `
            -AccountPassword  (ConvertTo-SecureString 'Pa$$word1' -AsPlainText -Force) `
            -UserPrincipalName "$uname@testsolutions.com" `
            -SamAccountName   $uname `
            -Enabled          $enabled `
            -Path             $user.DistinguishedName `
            -ErrorAction Stop

        if (-not [string]::IsNullOrWhiteSpace($user.Groups)) {
            foreach ($group in $user.Groups.Split(';')) {
                Add-ADGroupMember -Identity $group.Trim() -Members $uname -ErrorAction Stop
            }
        }

        Write-Host "SUCCESS: $uname ($display) created" -ForegroundColor Green
    }
    catch {
        $failed = if ($uname) { $uname } else { "$($user.FirstName) $($user.LastName)" }
        Write-Host "FAILED: $failed - $($_.Exception.Message)" -ForegroundColor Red
        if ($uname) { $script:CreatedUsernames.Remove($uname) }
    }
}
```

****Code by Claude (Since I have already provided it with the pseudo code and error handling and check)

#### Moving the Disabled users to the disabled OU* 

```Powershell
Import-Module ActiveDirectory

### Searching the active directory for the disabld 
Search-ADAccount -AccountDisabled  | Where {$_.DistinguishedName -notlike "*OU=Disabled Users,OU=Disabled Objects,OU=testsolutions,DC=testsolutions,DC=com"}|Move-ADObject -TargetPath "OU=Disabled Users,OU=Disabled Objects,OU=testsolutions,DC=testsolutions,DC=com"

### Marking the User as inactive
Get-ADUser -Filter {Enabled -eq $true} -SearchBase "OU=Disabled Users,OU=Disabled Objects,OU=testsolutions,DC=testsolutions,DC=com" | Disable-ADAccount
 
```


![](../Attachments/Pasted%20image%2020260212094535.png)






