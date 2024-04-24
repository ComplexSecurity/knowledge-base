Asynchronous SQL injection is a form of [[SQL injection]] attack where the malicious SQL commands executed by an attacker don't produce immediate results. 

In traditional SQL injection, the attacker inputs malicious SQL code into an input field (like a search box or login form) to manipulate a database in ways that benefit them, such as accessing unauthorized data. 

The results of these actions are typically immediate and directly observable by the attacker, such as retrieving hidden data or altering database content.

In contrast, with asynchronous SQL injection, the effects of the malicious SQL commands might not be immediately visible. These attacks might involve injecting a payload that is executed at a later time or under certain conditions, making detection and prevention more challenging. 

For example, the payload might be designed to trigger when a specific event occurs in the database or application, or it might execute in a background process that doesn't provide direct output to the attacker.

This type of attack requires a more sophisticated approach both in execution and in detection. It's also more difficult to trace, as the delayed execution can disconnect the cause (injection) from the effect (malicious action), complicating efforts to identify and mitigate the attack.