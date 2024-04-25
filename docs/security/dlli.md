DLL Injection is a technique used in software development and cybersecurity, including penetration testing, where a Dynamic Link Library ([[DLLs|DLL]]) file is loaded into the address space of another process by force. This action causes the targeted process to run the code contained in the DLL file.

The first step is to identify a target process into which the DLL will be injected. The injector process (controlled by the attacker or pentester) allocates memory within the target process’s address space, usually using functions like [[VirtualAllocEx]]. The path of the DLL to be injected is written to the allocated memory space in the target process.

The injector process then creates a new thread in the target process that calls functions like [[LoadLibrary]], which load the DLL from the path written into memory. Once the DLL is loaded into the target process's address space, the code within the DLL executes as if it were a part of the target process.
