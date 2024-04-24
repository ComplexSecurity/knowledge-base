icon:simple/windows10

# Net User

Command-line utility in Windows used to manage local or domain user accounts, allowing administrators to create, modify, or delete user accounts and manage user properties.

## Usage

```powershell
net user
```

## Flags

```powershell
[username [password | *] [options]] [/DOMAIN]
         username {password | *} /ADD [options] [/DOMAIN]
         username [/DELETE] [/DOMAIN]
         username [/TIMES:{times | ALL}]
         username [/ACTIVE: {YES | NO}]
```

## Examples

##### Show users on local system

```powershell
net user
```

##### Show users available in domain

```powershell
net user /DOMAIN
```

##### Show specific domain user information

```powershell
net user JohnDo /domain
```

##### Add user to domain

```powershell
net user JohnDo /ADD
```

##### Add user to group

```powershell
net group "Domain Admins" JohnDo /ADD /DOMAIN
```

## References

- [Docs.microsoft.com](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/cc771865%28v%3Dws.11%29)
