icon:fontawesome/solid/terminal

# Sudo

Command-line utility that allows users to execute commands as another user, typically the superuser or root.

## Usage

```bash
sudo -h | -K | -k | -V
sudo -v [-ABknS] [-g group] [-h host] [-p prompt] [-u user]
sudo -l [-ABknS] [-g group] [-h host] [-p prompt] [-U user] [-u user] [command]
sudo [-ABbEHknPS] [-r role] [-t type] [-C num] [-D directory] [-g group] [-h host] [-p prompt] [-R directory] [-T timeout] [-u user] [VAR=value] [-i|-s] [<command>]
sudo -e [-ABknS] [-r role] [-t type] [-C num] [-D directory] [-g group] [-h host] [-p prompt] [-R directory] [-T timeout] [-u user] file ...
```

## Flags

```bash
Options:
  -A, --askpass                 use a helper program for password prompting
  -b, --background              run command in the background
  -B, --bell                    ring bell when prompting
  -C, --close-from=num          close all file descriptors >= num
  -D, --chdir=directory         change the working directory before running command
  -E, --preserve-env            preserve user environment when running command
      --preserve-env=list       preserve specific environment variables
  -e, --edit                    edit files instead of running a command
  -g, --group=group             run command as the specified group name or ID
  -H, --set-home                set HOME variable to target user's home dir
  -h, --help                    display help message and exit
  -h, --host=host               run command on host (if supported by plugin)
  -i, --login                   run login shell as the target user; a command may also be specified
  -K, --remove-timestamp        remove timestamp file completely
  -k, --reset-timestamp         invalidate timestamp file
  -l, --list                    list user's privileges or check a specific command; use twice for longer format
  -n, --non-interactive         non-interactive mode, no prompts are used
  -P, --preserve-groups         preserve group vector instead of setting to target's
  -p, --prompt=prompt           use the specified password prompt
  -R, --chroot=directory        change the root directory before running command
  -r, --role=role               create SELinux security context with specified role
  -S, --stdin                   read password from standard input
  -s, --shell                   run shell as the target user; a command may also be specified
  -t, --type=type               create SELinux security context with specified type
  -T, --command-timeout=timeout terminate command after the specified time limit
  -U, --other-user=user         in list mode, display privileges for user
  -u, --user=user               run command (or edit file) as specified user name or ID
  -V, --version                 display version information and exit
  -v, --validate                update user's timestamp without running a command
  --                            stop processing command line arguments
```

## Examples

##### List privileges

Shown in the following example, the user bob can only run /usr/bin/bash with sudo privileges, no password is required furthermore.

```bash
$ sudo -l
Matching Defaults entries for bob on kali:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin, use_pty

User bob may run the following commands on kali:
    (ALL) NOPASSWD: /usr/bin/bash
```

The next listing shows all sudo privileges are present for the user bob.

```bash
$ sudo -l
[sudo] password for bob:
Matching Defaults entries for bob on kali:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin, use_pty

User bob may run the following commands on kali:
    (ALL : ALL) ALL
```

## References

- [Linux.die.net](https://linux.die.net/man/8/sudo)
