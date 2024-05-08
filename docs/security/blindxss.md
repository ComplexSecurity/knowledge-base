Blind [Cross-Site Scripting]() (XSS) is a subset of the more widely known Cross-Site Scripting vulnerability, specifically [Stored (Persistent) XSS|Stored XSS](), but with a key difference in its discovery and exploitation. 

In a standard XSS attack, the attacker's payload (malicious script) is executed immediately in the user's browser and the results are instantly observable by the attacker. However, in a Blind XSS attack, the exploitation is not immediately visible.

The attacker injects a malicious script into areas of a web application that are not immediately rendered or presented back to the user. Common injection points include fields that store data, like user profiles, comments, feedback forms, and support tickets.

The injected script lies dormant and is not executed immediately. Instead, it waits until an internal user, such as a support staff member or administrator, views the data containing the script.

When the internal user views the data, the script executes. This could potentially happen within an administrative or privileged user interface, which is not accessible to the attacker directly. The script, once executed, can perform actions such as stealing cookies, session tokens, or sensitive information from the internal user's browser, or even carry out actions on their behalf.

