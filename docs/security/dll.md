DLL hijacking is a vulnerability exploitation technique where an attacker exploits the way some Windows applications search for and load Dynamic Link Libraries ([DLLs]()). If an application does not specify a full path for a DLL, Windows searches for the DLL in a predefined set of directories.

An attacker can place a malicious DLL with the expected name in a directory that is searched before the legitimate one, leading the application to load the attacker's DLL instead of the legitimate one.

When an application needs to load a DLL, it often searches for the file in a set of default directories if the full path is not specified. The attacker places a malicious DLL with the same name as the legitimate DLL in a directory that the application searches before the legitimate DLL directory. When the application runs, it inadvertently loads the attacker's malicious DLL, executing the code within it.

Some examples may include:

- **Hijacking System Utilities**: An attacker places a malicious version of a commonly used DLL in a directory that is part of the system PATH. When a system utility is executed, it loads the malicious DLL, giving the attacker control or additional access.
- **Exploiting Third-party Applications**: Many third-party applications do not use full paths to load DLLs. By placing a malicious DLL in the application's directory or another directory in the search path, attackers can exploit this behavior.
- **Bundled Software**: Software that comes bundled with other applications might search for a DLL in its own directory first. If an attacker replaces one of these DLLs with a malicious version, it can lead to the execution of malicious code.
