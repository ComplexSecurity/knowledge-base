icon:simple/windows10

# AzureAD

Azure Active Directory (AzureAD) is Microsoft's cloud-based identity and access management service, providing authentication and authorization functionalities for cloud-based applications and services.

Please check Roadrecon, MFASweep, AzureHound and [Azure Active Directory - Rootsecdev](https://github.com/rootsecdev/Azure-Red-Team)

## Files

[Presentation from Antonio Formato of Cyber Saiyan - Hands [off_on] MS Cloud Services.pdf](../assets/files/Hands%20[off_on]%20MS%20cloud%20services.pdf){:download="Hands [off_on] MS Cloud Services.pdf"}

## Installation

```powershell
Install-Module AzureAD
```

## Usage

First step is to authenticate

```powershell
$AzureAdCred = Get-Credential
Connect-AzureAD -Credential $AzureAdCred
```

## Examples

##### Get-AzureADUser

```powershell
PS C:\Users\Commando-B > Get-AzureADUser

ObjectId                             DisplayName               UserPrincipalName                       UserType
--------                             -----------               -----------------                       --------
cb404750-4ae1-[REDACTED]             John Do                   john.do@offsec.nl                      Member
b4e1ee94-0ad8-[REDACTED]             Jane DO                   jane.do@offsec.nl                      Member
d2a782cb-838e-[REDACTED]             Administrator             admin@offsec.nl.onmicrosoft.com           Member
```

##### Get-AzureADGroup

```powershell
PS C:\Users\Commando-B > Get-AzureADGroup

ObjectId                             DisplayName                        Description
--------                             -----------                        -----------
005863b2-5fea-[REDACTED]             Testgroup 1                        Just a test group
00ad7bf9-f06d-[REDACTED]             Testgroup 2                        Just another test group
```

## References

- [posts.specterops.io](https://posts.specterops.io/requesting-azure-ad-request-tokens-on-azure-ad-joined-machines-for-browser-sso-2b0409caad30?gi=7d52b34697d0)
- [DirkJanM.io PrivEsc](https://dirkjanm.io/azure-ad-privilege-escalation-application-admin/)
- [DirkJanM.io RoadRecon](https://dirkjanm.io/introducing-roadtools-and-roadrecon-azure-ad-exploration-framework/)
