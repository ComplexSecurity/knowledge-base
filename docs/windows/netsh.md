icon:simple/windows10

# Netsh

Command-line utility in Windows used to manage network configurations, including interfaces, firewall settings, and routing tables.

## Usage

```powershell
netsh [OPTIONS]
```

## Flags

```powershell
Commands in this context:
..             - Goes up one context level.
?              - Displays a list of commands.
abort          - Discards changes made while in offline mode.
add            - Adds a configuration entry to a list of entries.
advfirewall    - Changes to the `netsh advfirewall' context.
alias          - Adds an alias.
branchcache    - Changes to the `netsh branchcache' context.
bridge         - Changes to the `netsh bridge' context.
bye            - Exits the program.
commit         - Commits changes made while in offline mode.
delete         - Deletes a configuration entry from a list of entries.
dhcpclient     - Changes to the `netsh dhcpclient' context.
dnsclient      - Changes to the `netsh dnsclient' context.
dump           - Displays a configuration script.
exec           - Runs a script file.
exit           - Exits the program.
firewall       - Changes to the `netsh firewall' context.
help           - Displays a list of commands.
http           - Changes to the `netsh http' context.
interface      - Changes to the `netsh interface' context.
ipsec          - Changes to the `netsh ipsec' context.
lan            - Changes to the `netsh lan' context.
mbn            - Changes to the `netsh mbn' context.
namespace      - Changes to the `netsh namespace' context.
netio          - Changes to the `netsh netio' context.
offline        - Sets the current mode to offline.
online         - Sets the current mode to online.
p2p            - Changes to the `netsh p2p' context.
popd           - Pops a context from the stack.
pushd          - Pushes current context on stack.
quit           - Exits the program.
ras            - Changes to the `netsh ras' context.
rpc            - Changes to the `netsh rpc' context.
set            - Updates configuration settings.
show           - Displays information.
trace          - Changes to the `netsh trace' context.
unalias        - Deletes an alias.
wcn            - Changes to the `netsh wcn' context.
wfp            - Changes to the `netsh wfp' context.
winhttp        - Changes to the `netsh winhttp' context.
winsock        - Changes to the `netsh winsock' context.
wlan           - Changes to the `netsh wlan' context.

The following sub-contexts are available:
 advfirewall branchcache bridge dhcpclient dnsclient firewall http interface ipsec lan mbn namespace netio p2p ras rpc trace wcn wfp winhttp winsock wlan
```

## Examples

##### Shown known Wi-Fi networks

```powershell
netsh wlan show profile
```

##### Show passwords from known networks (admin privs)

```powershell
netsh wlan show profile "<profilename>" key=clear
```

A script for showing all known network passwords quickly:

- [Show_All_Wifi_Password.ps1](../assets/files/Show_All_WiFi_Password.ps1)

```powershell
$Profiles=@()
$Profiles +=(netsh wlan show profiles) | Select-String "\:(.+)$" | Foreach{$_.Matches.Groups[1].Value.Trim()}
$Profiles | Foreach{$SSID = $_ ; (netsh wlan show profile name="$_" key=clear)} |
            Select-String "Key Content\W+\:(.+)$" |
                Foreach{$pass=$_.Matches.Groups[1].Value.Trim(); $_} |
                    Foreach{[PSCustomObject]@{Wireless_Network_Name=$SSID;Password=$pass}}
                        Format-Table -AutoSize
Start-Sleep -s 20
```

##### Show current IP configuration

```powershell
$ netsh interface ip show config

Configuration for interface "Ethernet"
    DHCP enabled:                         Yes
    IP Address:                           10.0.2.15
    Subnet Prefix:                        10.0.2.0/24 (mask 255.255.255.0)
    Default Gateway:                      10.0.2.2
    Gateway Metric:                       0
    InterfaceMetric:                      25
    DNS servers configured through DHCP:  10.0.2.3
    Register with which suffix:           Primary only
    WINS servers configured through DHCP: None
```

##### Create mobile hotspot

```powershell
netsh wlan set hostednetwork mode=allow ssid=Test key=12345678
```

Start the Mobile hotspot with **netsh wlan start hostednetwork**

##### Show current firewall configuration

```powershell
$ netsh advfirewall show currentprofile

Public Profile Settings:
----------------------------------------------------------------------
State                                 ON
Firewall Policy                       BlockInbound,AllowOutbound
LocalFirewallRules                    N/A (GPO-store only)
LocalConSecRules                      N/A (GPO-store only)
InboundUserNotification               Enable
RemoteManagement                      Disable
UnicastResponseToMulticast            Enable

Logging:
LogAllowedConnections                 Disable
LogDroppedConnections                 Disable
FileName                              %systemroot%\system32\LogFiles\Firewall\pfirewall.log
MaxFileSize                           4096

Ok.
```

List all firewall rules currently active: **netsh advfirewall firewall show rule name=all**

##### Remote Port Forwarding

- **v4tov4** - Makes sure IPv4 to IPv4 routing is done.
- **listenport** - Port to listen on the local host.
- **listenaddress** - IP address to listen on local machine.
- **connectport** - The local port that is forwarded listenport.
- **connectaddress** - The remote host to connect the session to.

```powershell
netsh interface portproxy add v4tov4 listenport=1234 listenaddress=192.168.1.1 connectport=445 connectaddress=10.10.10.1
```

**NOTE default firewall rules will not allow 1234 to direct traffic outbound. The command below creates the allow rule.**

```powershell
netsh advfirewall firewall add rule name="forward_port_rule" protocol=TCP dir=in localip=192.168.1.1 localport=1234 action=allow
```

## References

- [Docs.microsoft.com](https://docs.microsoft.com/nl-nl/windows-server/networking/technologies/netsh/netsh)
