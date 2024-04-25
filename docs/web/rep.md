REP stands for Robots Exclusion Protocol, a group of web standards that govern how robots (such as [[Search Engine Crawlers]]) crawl the web, access and index content, and serve that content up to users. The protocol consists of standards and practices that website administrators use to regulate the behavior of robots and web crawlers to prevent overloading their sites and to keep certain parts of their sites private.

The primary content of REP is the "[[Robots.txt]]" file. It's a text file placed at the root of a website (e.g., `https://example.com/robots.txt`) that provides instructions to web crawlers about which parts of the site should or shouldn’t be crawled and indexed. The file uses a simple syntax to indicate allowed and disallowed paths for user agents (crawlers).

Meta tags in [[HTML]] documents can be used to control crawler access on a page-by-page basis. For example, a `<meta name="robots" content="noindex">` tag tells crawlers not to index that specific page.

The "X-Robots-Tag" header is used to control how specified parts of a website are indexed, similar to the meta tags but can be applied to any HTTP-served content, not just HTML pages. 

While not strictly part of the REP, sitemaps are often used in conjunction with `robots.txt` to guide crawlers to the content that should be indexed. They provide structured information about the pages on the site, their relative importance, and how often they are updated.

While REP can be used to ask crawlers not to index certain parts of a site, it is not a security measure. Anything sensitive should not be left unprotected on the assumption that a `robots.txt` file will keep it hidden. The structure of a `robots.txt` file can inadvertently reveal the presence of sensitive directories or pages to potential attackers.
