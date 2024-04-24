icon:simple/windows10

# Net Group

Command-line utility in Windows used to manage local or domain user groups, allowing administrators to create, modify, or delete groups and manage group memberships.

## Usage

```powershell
net group [OPTIONS]
```

## Flags

```powershell
net group [<GroupName> [/comment:"<Text>"]] [/domain]
net group [<GroupName>{/add [/comment:"<Text>"] | /delete} [/domain]]
net group [<GroupName> <UserName>[ ...] {/add | /delete} [/domain]]
```

## Examples

##### Show all members of a specific group

```powershell
net group "Domain Admins" /DOMAIN
```

```powershell
The request will be processed at a domain controller for domain example.local.

Group name     Domain Admins
Comment        Designated administrators of the domain

Members

-------------------------------------------------------------------------------
JohnDO
The command completed successfully.
```

##### List all domain groups

```powershell
net group /DOMAIN
```

```powershell
The request will be processed at a domain controller for domain example.local.


Group Accounts for \\example.local

-------------------------------------------------------------------------------
*Cloneable Domain Controllers
*Compliance Management
*Delegated Setup
*Discovery Management
*DnsUpdateProxy
*Domain Admins
*Domain Computers
*Domain Controllers
*Domain Guests
*Domain Users
[...]
```

## References

- [Docs.microsoft.com](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/cc754051%28v=ws.11%29)
