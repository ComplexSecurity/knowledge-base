HSQLDB (HyperSQL DataBase) is an open-source [[relational database management system]] written in [[Java]]. It offers a small, fast, multithreaded and transactional database engine with in-memory and disk-based tables and supports embedded and server modes. HSQLDB is known for its compact size, high performance, and robust feature set.

HSQLDB is lightweight, requiring minimal resources to run, which makes it an ideal choice for applications that need a small, embedded database system. Since it's written in Java, HSQLDB can be easily integrated into Java applications. It is often used for development, testing, and deployment of Java applications.

One of HSQLDB's notable features is its ability to create in-memory databases, which reside entirely in the memory of the host application, offering very high query and update performance.

Besides in-memory databases, HSQLDB also supports traditional disk-based databases, which are more suitable for larger data sets or when data persistence is required. HSQLDB can be run in an embedded mode, where the database engine runs in the same process as the application, or in a server mode, which supports multi-user connectivity.

HSQLDB is highly [[Structured Query Language|SQL]]-compliant. It supports a large subset of SQL-92, SQL-99, and SQL-2008 standards along with SQL/MED extensions for Java functions and stored procedures.

HSQLDB offers full ACID (Atomicity, Consistency, Isolation, Durability) compliance for transactional processing, ensuring the reliability and integrity of data. While primarily designed for lightweight applications, HSQLDB performs well with larger data sets and can be scaled for more demanding environments.

HSQLDB provides tools for data export and import, allowing easy migration to and from other database systems. It is used in a variety of applications, from small web applications and desktop applications to large enterprise systems requiring a robust database backend.