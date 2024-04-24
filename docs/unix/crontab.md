icon:fontawesome/solid/terminal

# Crontab

Command-line utility used to schedule automated tasks by editing the crontab file, which specifies shell commands to run periodically on a given schedule.

## Usage

```bash
crontab [-u user] file
```

## Flags

```bash
usage: crontab [-u user] file
crontab [ -u user ][ -i ] { -e | -l | -r }
(default operation is replace, per 1003.2)
-e (edit user's crontab)
-l (list user's crontab)
-r (delete user's crontab)
-i (prompt before deleting users crontab)
```

## Examples

##### List tasks for current user

```bash
crontab -l
```

##### List tasks for other user

```bash
sudo crontab -l -u <user>
```

##### Edit tasks for current user

```bash
crontab -e
```

##### Edit tasks for other user

```bash
sudo crontab -e -u <user>
```

## Crontab Time Notation

```bash
Five asterix * * * * *
First   * : minutes (0-59)
Second  * : hours (0-23)
Third   * : day of the month (1-31)
Fourth  * : month (1-12)
Fifth   * : day of the week (0-6 or 1-7)
```

## References

- [Crontab.guru](https://crontab.guru/)
