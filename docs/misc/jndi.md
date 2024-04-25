The Java Naming and Directory Interface (JNDI) is an Application Programming Interface ([[APIs|API]]) provided by Java for connecting a [[Java]] application to multiple naming and directory services. It is part of the Java Platform, Standard Edition (Java SE) and Java Platform, Enterprise Edition (Java EE). 

JNDI plays a crucial role in enterprise applications, where it's used for looking up data and resources, such as database connections, environment entries, and Java objects, in a way that's abstracted from the underlying implementation.

JNDI provides a unified interface to multiple naming and directory services, allowing Java applications to access these services in a uniform way, regardless of the actual implementation of the service.

It can be used with various directory and naming services like LDAP ([[Lightweight Directory Access Protocol]]), [[DNS]] (Domain Name System), RMI ([[Remote Method Invocation]]) registries, and more.

In Java EE applications, JNDI is commonly used to look up resources like data sources (for database connections), [[Java Messaging Service (JMS)]] resources, [[Enterprise JavaBeans (EJBs)]], and environment variables defined in the deployment descriptor.

JNDI has a pluggable architecture, allowing different service providers to be plugged in seamlessly. This makes it extensible and adaptable to various service types. The `Context` and `InitialContext` classes in JNDI are used to look up objects in a naming directory. The `InitialContext` acts as the starting point for a naming operation.

By using JNDI, Java applications achieve portability across different environments, as they don't depend on a specific directory or naming service implementation. JNDI allows Java objects to be bound (assigned) to a name that can be later used for lookup. Similarly, objects can be unbound (removed) from names.

JNDI is often used in conjunction with other Java EE technologies like [[Java Messaging Service (JMS)|JMS]], [[JDBC]], and [[Enterprise JavaBeans (EJBs)|EJB]], providing a mechanism to retrieve objects that are managed by the application server.