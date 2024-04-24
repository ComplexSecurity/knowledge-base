Apache Derby, an [[Apache]] DB subproject, is a [[relational database management system]] (RDBMS) implemented entirely in [[Java]]. Known for its small footprint, ease of use, and embeddable nature, it's particularly well-suited for development, testing, and deployment of Java applications.

Being written in Java, Derby can be easily embedded in Java applications. It runs within the Java Virtual Machine (JVM) of the application it supports, making deployment and management relatively straightforward.

One of Derby's main features is its ability to be embedded into a Java application. In embedded mode, the database runs within the same JVM as the application and is invisible to the user.

Derby is lightweight, with a disk footprint of about 3.5MB for the base engine and embedded JDBC driver. This makes it an excellent choice for applications where a full-scale DBMS would be unnecessary or cumbersome.

Apart from being embedded, Derby can also run in a stand-alone server mode. In this mode, the database is accessible from other JVMs running on different machines.

Derby supports a significant subset of SQL and JDBC standards. It allows developers to use standard SQL queries and JDBC APIs for database operations. Derby supports transactions and is ACID-compliant (Atomicity, Consistency, Isolation, Durability), ensuring reliable data processing and integrity.

It offers a reasonable level of security, including user authentication and authorization. Derby also supports encrypted database files. Derby can run as an in-memory database, which is useful for applications that require fast data access and where data persistence between restarts is not necessary.

From being embedded in open-source projects and commercial products to being used for small web applications, Derby's flexibility makes it suitable for a wide range of use cases.

Apache Derby is open source and free to use. It benefits from community support, regular updates, and a pool of developers who contribute to its ongoing development.