Fuzz testing or fuzzing is an automated software testing method that injects invalid, malformed, or unexpected inputs into a system to reveal software defects and vulnerabilities.

A fuzzing tool injects these inputs into the system and then monitors for exceptions such as crashes or information leakage.

Put more simply, fuzzing introduces unexpected inputs into a system and watches to see if the system has any negative reactions to the inputs that indicate security, performance, or quality gaps or issues.

In web apps, fuzzing is a method of sending malformed or abnormal data to a system in order to get it to misbehave in some way, which could lead to the discovery of vulnerabilities.

Finding hidden files, sending random data to forms, or even login attempts to web applications can be considered fuzzing.

[[Brute Force Attack|Brute forcing]] can be considered a part of fuzzing. In brute force, the attacker uses valid data, for example, to check if a login attempt works. But with Fuzzing, they can send random data to break the expected behavior of a system.

For example, if you use a tool like [[Ffuf]] and load it with hundreds of username-password combinations to try on a website, it is fuzzing. And that’s exactly what we will do using Ffuf.

Make sure you have written permission if you are going to try this tool on a third-party website.
