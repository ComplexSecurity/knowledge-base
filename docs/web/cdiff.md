Cross-domain iframes are [[HTML]] elements used in web development to embed content from a different domain (or website) into a webpage.

They represent a particular use of the \<iframe> tag in HTML, where the source of the iframe (the content it displays) comes from a domain that is different from the domain of the parent page.

Cross domain iframes provide a way to isolate embedded content from the parent page. This is particular useful for including third party content while maintaining a degree of separation from the main website's content.

Web browsers enforce the [[Same Origin Policy]], which restricts how documents or scripts loaded from one origin can interact with resources from another origin. In the context of iframes, this policy means that a script in an iframe from a different domain typically cannot directly access or modify the contents of the parent page.

While the isolation provided by cross-domain iframes can enhance security (by preventing third-party content from accessing sensitive data on the parent page), it also poses challenges. For instance, ensuring secure communication between the iframe and the parent page requires careful handling, often using postMessage [[APIs|API]] or other secure methods.

Sometimes, it's necessary for the embedded content in an iframe to communicate with the parent page or access resources from the parent domain. [[Cross-Origin Resource Sharing (CORS)]] is a mechanism that allows restricted resources on a web page to be requested from another domain outside the domain from which the first resource was served, under certain conditions.
