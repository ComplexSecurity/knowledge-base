# Absolute Paths

Absolute paths are a way of specifying the location of a file or directory in a file system, starting from the root directory.

The root directory is the topmost directory in a file system hierarchy. In Unix and Unix-like systems, it is denoted by a single forward slash (`/`), while in Windows systems, it typically starts with a drive letter followed by a colon and a backslash (e.g., `C:\`). An absolute path contains the complete address of a file or directory from the root directory. It doesn't depend on the current working directory of the user or application.

In Unix/Linux, an absolute path might look like `/home/username/Documents/file.txt`, where `/` is the root, and each `/` thereafter separates different levels of directories. In Windows, an absolute path might be `C:\Users\username\Documents\file.txt`, where `C:\` is the root drive, and each `\` separates different levels of directories.

Since absolute paths start from the root directory, they uniquely identify a file or directory's location in the file system, avoiding ambiguity. Absolute paths are particularly useful in scenarios where the relative position of files might change, or when a consistent and unchanging reference to a file is needed, like in system configuration or when linking libraries in programming.

[[Relative Paths]] specify a location starting from the current directory. They are shorter but depend on the current directory's location, making them less consistent for some uses compared to absolute paths.

!!! info
    For example, if your current directory is `/home/username`, a relative path to a file might be `Documents/file.txt`, which is relative to the current directory, whereas the absolute path would be `/home/username/Documents/file.txt`.

