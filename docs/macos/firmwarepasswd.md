icon:material/apple

# Firmwarepasswd

Command-line utility on macOS that manages firmware passwords, providing security by preventing unauthorized changes to startup disk settings.

## Usage

```bash
firmwarepasswd [OPTION]
```

## Flags

```bash
    ?                               Show usage
    -h                              Show usage
    -setpasswd                      Set a firmware password. You will be promted for passwords as needed.
                                        NOTE: if this is the first password set, and no mode is
                                            in place, the mode will automatically be set to "command"
    -setmode [mode] [-allow-oroms]  Set mode to:
                                        "command" - password required to change boot disk
                                        "full" - password required on all startups
                                        -allow-oroms permits option roms execution
                                        NOTE: cannot set a mode without having set a password
    -mode                           Print out the current mode setting
    -check                          Print out whether there is / isn't a firmware password is set
    -delete                         Delete current firmware password and mode setting
    -verify                         Verify current firmware password
    -unlockseed                     Generate a firmware password recovery key
                                        NOTE: Machine must be stable for this command to generate
                                            a valid seed.  No pending changes that need a restart.
                                        NOTE: Seed is only valid until the next time a firmware password
                                            command occurs.
    -disable-reset-capability       Disable firmware password reset using unlockseed
    -enable-reset-capability        Enable firmware password reset using unlockseed
                                        NOTE: cannot enable or disable firmware password reset
                                            without having set a password
```

## Examples

The firmware password can also be managed with the firmwarepasswd utility while booted into the OS. For example, to prompt for the firmware password when attempting to boot from a different volume:

```bash
sudo firmwarepasswd -setpasswd -setmode command
```

##### Verifying password

```bash
$ sudo firmwarepasswd -verify
Verifying Firmware Password
Enter password:
Correct
```

## References

- [Support.apple.com - Set a firmware password on your Mac](https://support.apple.com/en-us/HT204455)
