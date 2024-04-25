Web application mapping is a critical phase in web application security assessments, including penetration testing. It involves systematically analyzing a web application to understand its structure, functionality, and points of interaction.

This process is essential for identifying potential security vulnerabilities and planning targeted attacks to test the application's resilience against cyber threats.

Mapping out the structure of the application, including directories, files, and [[Uniform Resource Locator|URLs]] is a key aspect of mapping. This involves identifying the layout of the web application, the relationship between different pages, and how they are linked together.

You must also recognize all the entry points for user input, such as forms, query parameters, and [[HTTP headers]]. These entry points are crucial for subsequent stages of penetration testing, as they are often the target for injection attacks (like [[SQL injection]], [[Cross-Site Scripting|XSS]]).

Find all accessible resources on the web application, including hidden or less obvious directories, files, and [[APIs|APIs]]. This might involve using tools to crawl the application and uncover resources that are not linked from visible content.

Understand how the web application works, what each part does, and how different functions interact with each other. This includes understanding the business logic of the application to identify logic flaws.

Review how sessions are managed, including [[cookies]] and session tokens. This is important for identifying vulnerabilities in session handling that could be exploited.

Examine how the web application handles user authentication and authorization, to spot potential weaknesses or misconfigurations in access controls.

Identify the technologies used in the web application, such as the server-side platform, [[Databases (KB)|database]], and any frameworks or libraries. Knowledge of the technology stack is crucial for understanding the types of vulnerabilities that might be present.
