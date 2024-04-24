icon:fontawesome/solid/terminal

# Scp

Securely copies files between hosts on a network, using SSH for data transfer and authentication.

## Usage

```bash
scp [OPTIONS]
```

## Flags

```bash
usage: scp [-346BCpqrTv] [-c cipher] [-F ssh_config] [-i identity_file]
            [-J destination] [-l limit] [-o ssh_option] [-P port]
            [-S program] source ... target
```

## Examples

##### Transfer file to target (SSH)

```bash
scp <file> <user>@<ip-address>:~/
```

##### Receive file from target (SSH)

```bash
scp <user>@<ip-address>:~/<file> .
```

##### Receive file with key and specific port

```bash
scp -i ~/key.pub -P2222 john@10.10.10.10:~/hashes.ntds .
```

##### Send file with key

```bash
scp -i ~/key.pub hashes.zip proxy:~/
```

##### Copy all files in directory

```bash
scp <user>@<ip-address>:/directory/* .
```

##### Copy directory recursively from remote server

```bash
scp -r <user>@<ip-address>:/directory local_directory
```

## References

- [Linux.die.net](https://linux.die.net/man/1/scp)
