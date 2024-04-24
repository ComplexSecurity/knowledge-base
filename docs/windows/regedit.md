icon:simple/windows10

# Regedit

Graphical registry editor in Windows used to view, modify, and manage the Windows Registry, which stores configuration settings and options for the operating system and installed applications.

## Disable Remote User Account Control (UAC)

1. Open regedit.exe (as Administrator)
2. Navigate to “HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System”
3. Right-click in the blank area in the right pane and select New > DWORD Value
4. Name the new value “LocalAccountTokenFilterPolicy”
5. Double-click on the newly created “LocalAccountTokenFilterPolicy” value
6. Type 1 into the “Value data” entry and click OK
7. Reboot the computer

If you want to change the value via CMD/PowerShell:

```powershell
reg add HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System /v LocalAccountTokenFilterPolicy /t REG_DWORD /d 1
```

In case remote access is mitigated thru **User Rights Assignment** you can use the following to disable this.

- [ntrights.exe](../assets/files/ntrights.exe){:download="ntrights.exe"}

```powershell
C:\temp>ntrights.exe -r SeDenyNetworkLogonRight -u "Local Account"
Revoking SeDenyNetworkLogonRight from Local Account   ... successful
```

## Extract SAM/SYSTEM/SECURITY from registry

You need an elevated command prompt.

```powershell
reg save hklm\system system
reg save hklm\sam sam
reg save hklm\security security
```

## References

- [Support.accessdata.com](https://support.accessdata.com/hc/en-us/articles/204150405-Disable-Remote-UAC)
