Linux environment variables are dynamic values that the operating system and other applications use to determine information specific to an environment, such as the location to store files, the current user name, and which directory to find executable files. 

These variables are part of the environment in which a process runs and are used to pass information into and out of programs running on the shell.

Environment variables can be global (system-wide) or local (user-specific). System-wide variables apply to all users, whereas user-specific variables apply only to the particular user's environment. Some common variables include:

- `PATH`: Specifies the directories where executable files are located. When a command is entered, the system searches these directories in the order listed in the `PATH` variable.
- `HOME`: Indicates the current user's home directory.
- `USER`: Contains the username of the current user.
- `SHELL`: Specifies the path to the default shell.
- `PWD`: Represents the current working directory.
- `LANG`: Specifies the system language and locale.
- `EDITOR`: Sets the default text editor.
- `TZ`: Indicates the time zone.

Environment variables are accessed in the shell using the `$` prefix. For example, `echo $HOME` prints the current user's home directory. It's common to modify the `PATH` variable to add new directories to the search path. This allows executables in those directories to be run from anywhere without specifying the full path.

Child processes inherit the environment variables from their parent process. This behavior is essential for ensuring that system settings propagate correctly to all processes. Environment variables are widely used in shell scripts and applications to make them more flexible and adaptable to different system configurations.

Care must be taken with environment variables, particularly when used in scripts and applications, as they can be exploited if not properly handled (e.g., in cases of [Environment Variable Injection](../security/varinj.md)).