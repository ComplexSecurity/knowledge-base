WAR files (Web Application Archive files) are a type of [[Java Archive (JAR)]] file used to distribute and deploy web applications in the [[Java]] platform. The WAR file format is a standard packaging method for web applications that use servlets and [[JavaServer Pages (JSP)]].

WAR files are used to package web applications so that they can be easily deployed on any Java EE (Enterprise Edition) compliant server, like [[Apache Tomcat]], [[IBM WebSphere]], [[Oracle WebLogic]], etc.

A typical WAR file includes [[Java Servlets]], [[JavaServer Pages (JSP)|JSP files]], [[HTML]] pages, [[JavaScript]] files, [[CSS]] files, images, Java classes, [[Extensible Markup Language|XML]] configuration files, and any libraries required by the application (packaged as JAR files).

WAR files have a specific directory structure. The root of the WAR file contains JSP files, HTML files, and other resources accessible directly by clients. There is a special directory named `WEB-INF` which contains:

- `web.xml`: The deployment descriptor file that describes the servlets and other components of the application.
- `classes`: A directory for compiled Java class files.
- `lib`: A directory containing Java Archive (JAR) files that the web application depends on.
- Other configuration files and resources used by the application.

To deploy a web application, you typically copy the WAR file into a specific directory on the application server (like the `webapps` directory in Apache Tomcat). The server then automatically deploys the web application based on the contents of the WAR file.

WAR files simplify the deployment process, as they contain all the components of the web application in a single file. They provide a standard, server-agnostic way of packaging web applications, ensuring compatibility across different Java EE servers.

WAR files can be created manually by organizing files into the required structure and using a zip tool, or automatically using build tools like [[Apache Maven]], [[Gradle]], or [[Ant]].
