Dropwizard is an open-source [[Java]] framework for developing high-performance, [[REST APIs|RESTful]] web services and microservices. It is designed to be simple, fast, and easy to use, enabling developers to quickly bootstrap and deploy web applications.

Dropwizard glues together several mature and stable Java libraries to provide a comprehensive and efficient platform for building RESTful web applications. Dropwizard focuses on being lightweight and providing just enough to get high-performance web services up and running with minimal effort.

It comes with a set of pre-configured, high-quality libraries, including [[Jetty]] for [[HTTP Protocol|HTTP]], [[Jersey]] for RESTful services, [[Jackson]] for [[JavaScript Object Notation|JSON]] processing, [[Metrics]] for monitoring, and [[JDBI|JDBI]] or Hibernate for database access.

One of the primary uses of Dropwizard is to develop RESTful web services. It simplifies this process with Jersey, which makes mapping Java objects to web resources a straightforward task. Dropwizard includes operational tools like Metrics, which provide powerful insights into the performance and health of the application.

It uses a [[YAML|YAML]] file for external configuration, allowing for easy adjustment of settings and parameters without changing the code. The framework emphasizes convention over configuration, leading to rapid development and deployment of services.

Dropwizard includes built-in support for sophisticated error handling and validation mechanisms. It provides support for basic authentication, [[Knowledge Base/OAuth]], and other security mechanisms to protect web services. While Dropwizard is designed to be simple, it also allows for customization and extensions, enabling developers to add functionality as needed.
