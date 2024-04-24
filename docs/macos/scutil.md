icon:material/apple

# Scutil

Command-line utility on macOS used to manage system configuration parameters and interact with the System Configuration database.

## Usage

```bash
scutil [OPTIONS]
```

## Flags

```bash
   scutil --prefs [preference-file]
        interactive access to the [raw] stored preferences.

   or: scutil [-W] -r nodename
   or: scutil [-W] -r address
   or: scutil [-W] -r local-address remote-address
        check reachability of node, address, or address pair (-W to "watch").

   or: scutil -w dynamic-store-key [ -t timeout ]
        -w      wait for presense of dynamic store key
        -t      time to wait for key

   or: scutil --get pref
   or: scutil --set pref [newval]
   or: scutil --get filename path key
        pref    display (or set) the specified preference.  Valid preferences
                include:
                        ComputerName, LocalHostName, HostName
        newval  New preference value to be set.  If not specified,
                the new value will be read from standard input.

   or: scutil --dns
        show DNS configuration.

   or: scutil --proxy
        show "proxy" configuration.

   or: scutil --nwi
        show network information

   or: scutil --nc
        show VPN network configuration information. Use --nc help for full command list

   or: scutil --allow-new-interfaces [off|on]
        manage new interface creation with screen locked.

   or: scutil --error err#
        display a descriptive message for the given error code
```

## Examples

##### Change system hostname/bonjour and computer name

System hostname:

```bash
sudo scutil --set HostName bob.local
```

Bonjour hostname:

```bash
sudo scutil --set LocalHostName bob
```

Computer name:

```bash
sudo scutil --set ComputerName bob
```

##### Show DNS configuration

```bash
scutil --dns
```

##### Show network information

```bash
scutil --nwi
```

## References

- [ss64.com - scutil](https://ss64.com/osx/scutil.html)
