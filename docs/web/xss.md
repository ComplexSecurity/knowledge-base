**Cross-site scripting** (also known as XSS) is a web security vulnerability that allows an attacker to compromise the interactions that users have with a vulnerable application. It allows an attacker to circumvent the [[Same Origin Policy|same origin policy]], which is designed to segregate different websites from each other.

Cross-site scripting vulnerabilities normally allow an attacker to masquerade as a victim user, to carry out any actions that the user is able to perform, and to access any of the user's data. If the victim user has privileged access within the application, then the attacker might be able to gain full control over all of the application's functionality and data.

Cross-site scripting works by manipulating a vulnerable web site so that it returns malicious [[JavaScript]] to users. When the malicious code executes inside a victim's browser, the attacker can fully compromise their interaction with the application.

Websites that do not validate user input before using them in their outputs are typically susceptible to XSS attacks. While various frameworks (such as [[ActiveX]], Flash, [[CSS]], and [[VBScript]]) are sensitive to XSS, dynamic websites commonly notice the attack since such sites mostly rely on JavaScript.

XSS attacks are of three types:

- [[Reflected XSS]]
- [[Stored XSS]]
- [[DOM-based XSS]]

You can confirm most kinds of XSS vulnerability by injecting a payload that causes your own browser to execute some arbitrary JavaScript. It's long been common practice to use the **alert()** function for this purpose because it's short, harmless, and pretty hard to miss when it's successfully called.

Unfortunately, there's a slight hitch if you use Chrome. From version 92 onward (July 20th, 2021), cross-origin iframes are prevented from calling **alert().** As these are used to construct some of the more advanced XSS attacks, you'll sometimes need to use an alternative PoC payload such as **print()**.
