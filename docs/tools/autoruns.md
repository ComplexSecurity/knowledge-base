Autoruns is a utility in the Microsoft [[Sysinternals Suite]] that comprehensively lists all programs and services configured to run automatically on a Windows system. This tool is incredibly detailed, showing auto-starting locations that traditional task managers and other utilities often miss.

Autoruns reveals all programs, drivers, services, shell extensions, codecs, scheduled tasks, and other software automatically launched at startup or login. Users can filter out standard Windows entries to focus on third-party auto-starting images, making it easier to spot potentially unwanted or malicious software. For each entry, Autoruns shows the associated registry or file path, helping in identifying where each auto-start item is configured.

Malware often establishes [[persistence]] by placing itself in startup locations. Autoruns can help identify these entries, which might be indicators of compromise. During incident response, Autoruns can be used to find and remove unauthorized auto-start configurations that might be part of a malware's persistence mechanism.

Attackers or penetration testers can use Autoruns to understand all programs running on a system automatically, helping in mapping out the environment and identifying targets for further exploitation. Attackers might use knowledge gained from Autoruns to place their malware in less commonly monitored auto-start locations, potentially evading detection by security software.

