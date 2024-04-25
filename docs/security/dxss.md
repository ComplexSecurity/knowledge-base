[[Document Object Model|DOM]]-based XSS vulnerabilities usually arise when [[JavaScript]] takes data from an attacker-controllable source, such as the URL, and passes it to a sink that supports dynamic code execution, such as **eval()** or **innerHTML**. This enables attackers to execute malicious JavaScript, which typically allows them to hijack other users' accounts.

To deliver a DOM-based XSS attack, you need to place data into a source so that it is propagated to a sink and causes execution of arbitrary JavaScript.

The most common source for DOM XSS is the URL, which is typically accessed with the window.location object. An attacker can construct a link to send a victim to a vulnerable page with a payload in the query string and fragment portions of the URL.

In certain circumstances, such as when targeting a 404 page or a website running PHP, the payload can also be placed in the path.

Since these attacks rely on the [[Document Object Model]], they are orchestrated on the client-side after loading the page. In such attacks, the HTML source code and the response to the attack remain unchanged, so the malicious input is not included in the server response. Since the malicious payload is stored within the client’s browser environment, the attack cannot be detected using traditional traffic analysis tools.

DOM-based XSS attacks can only be seen by checking the document object model and client-side scripts at runtime.

Fundamentally, attackers perform DOM-based Cross-site scripting attacks on applications with an executable path for data to travel from a source to a sink. Sources are JavaScript properties that can act as the location of malicious input.

These include **document.URL**, **document.referrer**, **location.search**, and **location.hash** among others. A sink is a location or function that executes the malicious function in an HTML rendering.

Example of sinks include: **eval**, **setTimeout**, **setInterval** and **element.innerHTML** among others.
