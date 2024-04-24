icon:simple/windows10

# Net View

Command-line utility in Windows used to display a list of available network resources or computers in a specified domain or workgroup

## Usage

```powershell
net view [options]
```

## Examples

##### List all shares including hidden

```powershell
net view \\<DNS-or-IP> /All
```

##### List all shares on different domain

```powershell
net view /DOMAIN:domainname
```

## References

- [ss64.com](https://ss64.com/nt/net-view.html)
