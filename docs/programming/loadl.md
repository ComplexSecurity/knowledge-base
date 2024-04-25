`LoadLibrary` is a function in the Windows API that loads a [[DLLs|Dynamic Link Library (DLL)]] into the calling process's address space. The function is widely used in legitimate software development to dynamically load libraries at runtime. However, in the context of hacking and [[DLL Hijacking]], `LoadLibrary` can be exploited for malicious purposes.

In a DLL injection attack, `LoadLibrary` is used to load a malicious DLL into a target process's memory. This is often achieved by first allocating memory in the target process (using functions like `VirtualAllocEx`) and then writing the path of the malicious DLL into this allocated space. 

A remote thread is created within the target process using `CreateRemoteThread`, with `LoadLibrary` as the start routine, pointing to the memory location where the DLL path is written. This causes the target process to load and execute the malicious DLL.

As an example, an attacker injects a DLL into a process running with higher privileges. The DLL is loaded using `LoadLibrary`, granting the attacker the same privileges as the target process.

If an application does not specify a full path for a required DLL, Windows searches for the DLL in a predefined set of directories. An attacker can place a malicious DLL with the same name as the expected DLL in one of these directories. When the application uses `LoadLibrary` to load the DLL, it inadvertently loads the attacker's malicious DLL.

As an example, a legitimate application attempts to load a commonly used DLL, but due to the search order, it ends up loading a malicious DLL placed by the attacker in a directory that is searched before the legitimate one.

