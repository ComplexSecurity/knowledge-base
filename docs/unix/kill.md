icon:fontawesome/solid/terminal

# Kill

Used to send signals to processes, typically for terminating them.

## Usage

##### Kill by PID

```bash
kill <pid>
```

##### Kill by name

```bash
pkill <name>
```

## Flags

```bash
-1  SIGHUP
-2  SIGINT
-9  SIGKILL
-15 SIGTERM
```

## References

- [Linux.die.net](https://linux.die.net/man/3/kill)
