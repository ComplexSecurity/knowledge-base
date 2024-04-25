In web application penetration testing (pentesting), a "whitelist" is a security mechanism that permits only predefined and explicitly allowed inputs, actions, or entities, while blocking everything else. Whitelisting is often considered a more secure, albeit more restrictive, approach compared to blacklisting.

Whitelists are commonly used for input validation. Web applications compare user inputs against a list of safe characters, strings, or patterns, accepting only those that are explicitly allowed.

Unlike [[Blacklists|blacklisting]], which attempts to enumerate all potentially harmful inputs (a near-impossible task), whitelisting ensures that only known-safe inputs are accepted. This reduces the risk of security bypasses due to unforeseen attack vectors.

Examples of whitelisting include allowing only alphanumeric characters in a user ID field, permitting specific file types in upload forms, or enabling only certain HTML tags in text inputs.

Determining what to include on the whitelist can be challenging, especially in complex applications where the range of legitimate inputs is broad. Overly restrictive whitelists may hinder application usability or functionality.

During pentesting, security testers attempt to bypass whitelists to assess their effectiveness. This involves crafting inputs that are technically on the whitelist but used in malicious ways.

Whitelisting is most effective when used as part of a layered security strategy, combined with other measures like secure coding practices, regular security reviews, and user education. The effectiveness of a whitelist often depends on its context. For instance, a whitelist in an email system might allow different inputs compared to a whitelist in a content management system.

In more advanced implementations, whitelists can be dynamic, adjusting the allowed inputs based on the application's state or user context.
