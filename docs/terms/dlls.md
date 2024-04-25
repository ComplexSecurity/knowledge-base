DLLs, or Dynamic Link Libraries, are modules of executable functions or routines that can be used by Windows applications and services. A DLL can be shared among multiple applications, providing a way to modularize code for efficiency and reusability. In the context of penetration testing and hacking, DLLs present both opportunities and vulnerabilities.

DLLs contain code that different programs can use simultaneously. Rather than having the same code in each program, a shared DLL can provide this functionality. Programs can use the functions and routines in a DLL as needed during runtime, which is known as dynamic linking. Windows operating systems come with numerous DLLs that provide essential functions, from basic file operations to network communication.

If an application improperly specifies the path to a DLL, an attacker can place a malicious DLL with the same name in a location that the application searches before the legitimate path. When the application runs, it loads the attacker’s DLL, executing malicious code - known as [[DLL Hijacking]].

[[DLL Injection]] involves injecting a DLL into a legitimate process's memory space. The injected DLL can then execute within the context of the process's permissions, potentially enabling privilege escalation or bypassing security controls.

You can also modify an existing DLL to include malicious code, which will be executed whenever the DLL is loaded by an application. Some applications might be vulnerable to attacks that manipulate the loading and unloading of DLLs, leading to crashes, [[Remote Code Execution|code execution]], or [[privilege escalation]].

You can also place a malicious DLL in a location from which a legitimate application loads additional components, leading to the execution of the malicious DLL.

Some examples include:

- **DLL Hijacking**: A penetration tester discovers that a third-party application does not specify the full path for a DLL it loads. The tester places a malicious DLL with the expected name in a directory that is searched before the legitimate DLL directory, leading to the execution of the tester’s code.
- **DLL Injection**: During a red team exercise, a tester injects a DLL into a process running with higher privileges. This DLL opens a backdoor, allowing the tester to access restricted areas of the network.

!!! info
    To defend against DLL-related attacks, it's important to use safe coding practices, regularly update applications and systems, monitor process behavior for unusual activity, and implement application whitelisting.
