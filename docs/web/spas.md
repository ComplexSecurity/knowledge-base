Single Page Applications (SPAs) are a type of web application or website that dynamically rewrite the current page rather than loading entire new pages from the server. This approach results in a smoother, more seamless user experience, similar to a desktop application. In an SPA, most of the necessary [[HTML]], [[JavaScript]], and [[CSS]] is either retrieved with a single page load or dynamically loaded and added to the page as necessary, usually in response to user actions.

In SPAs, much of the content is rendered on the client side (in the user's browser), using JavaScript. This means that after the initial page load, the SPA does not need to reload or refresh the whole page for most user interactions. 

SPAs heavily use [[AJAX]] (Asynchronous JavaScript and XML) to fetch data from the server asynchronously. This allows the application to request data in the background and update parts of the webpage without reloading the entire page. Since SPAs don't require full page reloads, they can provide a more fluid and app-like user experience, with less waiting time for page reloads.

The application consists of a single HTML page that gets dynamically updated. This single page acts as a shell for all the different views of the application.

Several JavaScript frameworks and libraries are popular for building SPAs, including:

- [[ReactJS|React]] (developed by Facebook)
- [[AngularJS|Angular]] (developed by Google)
- [[Vue.js]]
- [[Ember.js]]
- [[Backbone.js]]

Once loaded, SPAs can offer significantly faster interactions and smoother transitions, as only data, not entire pages, are exchanged with the server. Since much of the rendering is done client-side, SPAs can reduce the load on the server. SPAs can provide limited offline functionality, as the core application is already loaded in the browser.

Traditional SPAs may have issues with search engine optimization (SEO) since content is loaded dynamically, which can be problematic for web crawlers. The first load of an SPA can be slower since the browser may need to load more resources initially. Managing the application state can be more complex in SPAs compared to traditional multi-page applications.

SPAs are well-suited for applications where user experience and interactivity are priorities, such as social networks, SaaS platforms, and email clients. They are less suited for content-heavy sites where SEO is a primary concern.

There are a variety of different types of session attacks including:

- [[Session Hijacking]] - in session hijacking attacks, the attacker takes advantage of insecure session IDs, finds a way to obtain them, and uses them to authenticate to the server and impersonate the victim.
- [[Session Fixation]] - occurs when an attacker can fixate a valid session ID. The attacker will then have to trick the victim into logging into the application using the aforementioned session ID. If the victim does so, the attacker can proceed to a session hijacking attack (since the session ID is already known).
- [[Cross-Site Scripting]] - with a focus on user sessions
- [[Cross-Site Request Forgery]] - attack that forces an end-user to execute inadvertent actions on a web app in which they are currently authenticated. This attack is usually mounted with the help of attacker-crafted web pages that the victim must visit or interact with. These web pages contain malicious requests that essentially inherit the identity and privileges of the victim to perform an undesired function on the victim's behalf.
- [[Open Redirects]] - open redirects occur when an attacker can redirect a victim to an attacker-controlled site by abusing a legitimate application's redirection functionality. In such cases, all the attacker has to do is specify a website under their control in a redirection URL of a legitimate website and pass it to a victim. It is possible when the legitimate app's redirection functionality does not perform any kind of validation regarding the websites where the redirection points to.
