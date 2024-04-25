Relative paths are a way of specifying the location of a file or directory in relation to the current working directory in a file system.

A relative path is defined in relation to the current directory that the user or application is working in. This is known as the current working directory. Unlike [[Absolute Paths]], which provide the complete path from the root of the file system, relative paths navigate from the current directory. They do not start with the root directory or a drive letter.

In Unix/Linux, a relative path might look like `Documents/file.txt` or `../otherfolder/image.jpg`. The `.` denotes the current directory, and `..` denotes the parent directory. In Windows, similar to Unix/Linux but uses backslashes, like `Documents\file.txt` or `..\otherfolder\image.jpg`.

Relative paths are useful when the structure of a directory tree is consistent but the absolute position of the entire tree within the file system might change. For example, if a set of files is moved to a different folder or drive, relative paths inside this set will still be valid, whereas absolute paths would need updating.

Relative paths are commonly used in programming and web development to link files (like libraries, images, or other resources) that are within the same directory tree, as they allow for more portability of the code or website. 

Absolute paths provide a complete path from the root directory to the target file or directory and remain constant, regardless of the current working directory. Relative paths, being dependent on the current directory, are more flexible but can sometimes lead to confusion if the current directory context is not clear.

!!! info
    For example, if you are in the directory `/home/username/Documents`, and you want to refer to a file located at `/home/username/Pictures/image.jpg`, the relative path from your current directory would be `../Pictures/image.jpg`. This path means: go up one level to `/home/username/` (using `..`) and then down into `Pictures/image.jpg`.


