# Project 9: Domain Controller Setup

## Objective
Install Active Directory Domain Services (AD DS), configure a Domain Controller, and create two domain users to demonstrate basic authentication.

## Technologies Used
- Microsoft Azure
- Windows Server 2025
- Active Directory Domain Services (AD DS)
- DNS Server
- Windows PowerShell
- Azure Bastion

## Implementation

1. Created a Windows Server 2025 virtual machine named `p9-dc`.
2. Installed Active Directory Domain Services.
3. Promoted the Windows Server to a Domain Controller.
4. Created a new Active Directory forest named `lab.example.test`.
5. Configured DNS and verified Active Directory services.
6. Created two domain users:
   - `student1`
   - `student2`
7. Verified both users using `Get-ADUser`.
8. Tested domain authentication using PowerShell.

## Commands Used

Verify domain users:

```powershell
Get-ADUser -Identity student1
Get-ADUser -Identity student2
```

Verify services:

```powershell
Get-Service NTDS,DNS
```

Check domain details:

```powershell
Get-ADDomain
```

## Test Results

| Test | Result |
|---|---|
| AD DS installation | Passed |
| Domain Controller configuration | Passed |
| DNS service | Running |
| NTDS service | Running |
| student1 authentication | Passed |
| student2 authentication | Passed |

## Evidence

Screenshots demonstrate:
- Active Directory user creation
- Domain Controller service verification
- Successful credential authentication for both users

## Conclusion

Successfully installed and configured Active Directory Domain Services on Windows Server 2025 and verified authentication for two domain users.

**Note:** Credential authentication was verified successfully. Interactive login testing on a separate domain-joined Windows client remains pending.
