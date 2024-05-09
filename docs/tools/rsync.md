`rsync` (short for "remote synchronization") is a popular utility for efficiently transferring and synchronizing files across computer systems, using a network connection. It is widely used in Unix-like operating systems, including Linux and macOS, for tasks such as backups, mirroring, and copying files both locally and remotely.

`rsync` only transfers the changes or differences within files, rather than copying entire files. This differential transfer reduces the amount of data sent over the network, making it very efficient, especially for updating large files with small changes. It can be used to copy files both locally (on the same machine) and remotely (between different machines over a network).

`rsync` compresses data during transfer and can be used with [SSH]() for secure, encrypted data transfers. It can preserve various file attributes during transfer, such as timestamps, ownership, and permissions. The utility can delete files in the destination directory that are no longer present in the source directory, useful for maintaining exact mirrors.

`rsync` is commonly used for performing backups by copying files to external drives, network shares, or remote servers. It can mirror data from one server to another, ensuring that both locations have identical sets of files. For copying large sets of files or updating large files that have small changes.

Some example commands include a basic file copy:

```bash
rsync /path/to/source/file /path/to/destination
```

!!! info
    This command copies a file from the source to the destination directory.

Copying files to a remote server:

```bash
rsync /path/to/source username@remotehost:/path/to/destination
```

!!! info
    This command copies files from the local machine to a remote server using SSH.

For synchronizing directories:

```bash
rsync -av --delete /path/to/source/ /path/to/destination/
```

!!! info
    The `-a` flag preserves attributes, and `-v` provides verbose output. `--delete` removes files from the destination that are not in the source directory.

Or for creating an incremental backup:

```bash
rsync -av --link-dest=/path/to/previous/backup /path/to/source/ /path/to/current/backup
```

!!! info
    This creates an incremental backup, where only changes are stored, using hard links to unchanged files in the previous backup.

