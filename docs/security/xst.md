XST stands for Cross-Site Tracing, a network security vulnerability that combines [Cross-Site Scripting]() (XSS) with the [TRACE HTTP Method|HTTP TRACE method](). XST exploits the TRACE method supported by some web servers to bypass certain browser security mechanisms.

The TRACE method in HTTP is used for diagnostic purposes and echoes back the full request to the client. In an XST attack, the attacker exploits this functionality.

Normally, cookies marked as [HttpOnly Flag|HttpOnly]() cannot be accessed via [JavaScript](), which is a defense mechanism against XSS attacks. However, an XST attack can use the TRACE method to retrieve these `HttpOnly` cookies. The attacker typically injects a malicious script into a web page (XSS attack), and when the victim visits this page, the script forces their browser to issue a TRACE request to the server.

The server’s response to the TRACE request contains the victim's `HttpOnly` cookies and other header information in the body of the response. The malicious script then captures this information from the response.

By obtaining a user's session cookies, an attacker can hijack the user's session, gaining unauthorized access to their account. XST can bypass security mechanisms designed to protect against XSS, making it a significant threat.
