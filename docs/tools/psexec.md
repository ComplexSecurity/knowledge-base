Impacket's `psexec` is a script within the [Impacket](../tools/impacket.md) suite that emulates the functionality of [Microsoft's PsExec](../tools/mpsexec.md) tool. PsExec is a part of the [Sysinternals Suite](../tools/sysint.md) and allows execution of processes remotely by creating a service on the remote system. Impacket's `psexec` provides similar functionality, enabling users to execute commands or launch an interactive shell on remote Windows machines.

It allows for the execution of commands on a remote Windows machine. Users can spawn an interactive shell on the remote system, which is extremely useful for administration tasks or penetration testing scenarios. The script supports [NTLM](../security/ntlm.md) authentication, making it possible to authenticate against remote systems using either a password or an NTLM hash ([pass-the-hash](../activedirectory/pth.md)). `psexec` is widely used for legitimate network administration tasks and in penetration testing for gaining remote access to systems.

An example:

```bash
python psexec.py <DOMAIN>/<USERNAME>:<PASSWORD>@<TARGET_IP> cmd.exe
```

- `<TARGET_IP>` is the IP address of the target Windows machine.
- `cmd.exe` is the command to be executed on the remote system. This could be replaced with any command or even a path to an executable script.

If you wish to spawn an interactive shell, you might use the script without specifying a command:

```bash
python psexec.py <DOMAIN>/<USERNAME>:<PASSWORD>@<TARGET_IP>
```

