System Monitor, also known as Sysmon, is a utility provided by [Sysinternals](../tools/sysint.md) (now part of Microsoft) designed to monitor and log system activity to the Windows event log. It's a powerful tool often used in security monitoring and forensic analysis because it provides detailed information about process creations, network connections, and changes to file creation time.

Sysmon can log detailed information about process creations, network connections, driver loading, file creation, and more. This information is crucial for understanding the behavior of the system and identifying malicious or suspicious activity. 

Sysmon allows users to specify complex filtering rules, making it possible to capture only the relevant events. This helps in reducing the volume of logged data and focusing on potential security threats. Sysmon events are written to the Windows event log, which can be viewed using standard Windows tools like Event Viewer or integrated with central logging and [SIEM (Security Information and Event Management)](../security/siem.md) solutions.

Once installed and configured, Sysmon runs in the background as a Windows service, persistently monitoring the system for activity that matches its configuration rules.

Sysmon is widely used in cybersecurity for real-time monitoring of systems to detect signs of compromise or suspicious activity. During incident response, Sysmon data can provide valuable insights into what occurred on a system leading up to and during a security incident. Security professionals use Sysmon logs to hunt for indicators of compromise (IOCs) and tactics, techniques, and procedures (TTPs) used by attackers.

Consider a scenario where a company's IT department is alerted about potential malware activity on a networked computer. Sysmon, installed on the system, provides detailed logs showing:

- A previously unknown process was created.
- This process made suspicious network connections to an external server.
- The process also attempted to modify system files and registry keys.

