Single Page Application (SPA) Routing refers to the technique used in single-page applications to handle navigation between different sections of the application without the need for reloading the entire page from the server. 

In traditional web applications, navigating to different parts of the site involves requesting new pages from the server, which reloads the entire page content. In contrast, SPAs dynamically rewrite the current page in response to user actions, leading to a more fluid and responsive user experience.

In SPAs, routing is handled on the client side (in the user's browser) using [[JavaScript]]. When a user interacts with the application and requests a different part of the application (like a new page), the JavaScript intercepts the browser's navigation and handles the URL change without a full page reload.

Modern web applications often use the History API provided by browsers to manipulate the URL's path and query string. This allows SPA routing to maintain browser history (forward and back navigation) without reloading pages.

The application dynamically loads new content (usually in the form of [[HTML]], [[JavaScript Object Notation|JSON]], or [[Extensible Markup Language|XML]]) from the server and updates the existing page, rather than requesting entire new pages. Most SPA frameworks and libraries, such as [[AngularJS|Angular]], [[ReactJS|React]], [[Vue.js]], and others, have built-in routing solutions or popular routing libraries that manage the complexities of SPA routing, like Angular Router or React Router.

SPA routers manage deep links and allow users to bookmark specific states of the application. Historically, SPAs faced challenges with search engine optimization (SEO) due to their dynamic nature. Modern techniques and improvements in search engine technologies have largely mitigated these issues.

SPAs generally rely on JavaScript. Proper routing ensures that users without JavaScript or with JavaScript errors still have access to basic functionality, often through server-side rendering or pre-rendering strategies.