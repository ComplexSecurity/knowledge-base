Empire is a post-exploitation framework that is used primarily in penetration testing and red team operations. It provides a powerful platform for executing advanced post-exploitation tasks on compromised systems. Empire was originally developed as a [Windows PowerShell](../tools/ps.md) tool, which later expanded to include [Python](../programming/python.md) for Linux and macOS environments.

Empire is built around a modular framework, allowing users to execute a wide range of post-exploitation tasks through its various modules. Initially focused on PowerShell for Windows environments, Empire has evolved to support Python, extending its capabilities to Linux and macOS systems. It works by setting up agents on compromised systems. These agents communicate back to the Empire server, allowing for remote control and command execution.

Empire can be used to establish [command and control (C2)](../security/c2.md) channels, facilitating long-term access to compromised systems. The framework includes capabilities for [lateral movement](../security/lat.md), [privilege escalation](../security/privesc.md), [reconnaissance](../security/recon.md), [data exfiltration](../security/exfil.md), and more. It can be integrated with other penetration testing and cybersecurity tools, enhancing its functionality in complex security assessments.

In a typical penetration testing scenario, an attacker would use Empire to:

1. Gain initial access to a system, possibly through [phishing](../security/phishing.md) or exploiting a vulnerability.
2. Deploy an Empire agent on the compromised system.
3. Use the Empire console to execute modules for further exploitation, such as harvesting credentials, moving laterally across the network, and accessing sensitive data.
