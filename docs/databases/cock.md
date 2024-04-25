CockroachDB is a distributed [[Structured Query Language|SQL]] database designed for cloud-native and scalable applications. It provides horizontal scalability, strong consistency, and resilience, making it suitable for a wide range of applications that require reliable, available, and fault-tolerant data storage.

CockroachDB is designed to be a distributed database. It scales horizontally, meaning you can add more nodes to the system to increase capacity and throughput. One of the core features of CockroachDB is its strong resilience against failures. Data is automatically replicated across multiple nodes, which helps in ensuring high availability and protecting against server or data center outages.

It offers serializable isolation, which is the highest level of isolation in databases, ensuring strong consistency across distributed data. Transactions are atomic, consistent, isolated, and durable (ACID).

Despite being a [[Non-relational Database|NoSQL]] database in architecture, CockroachDB supports a full SQL interface for querying data, which makes it familiar and accessible to developers who are used to traditional SQL databases.

CockroachDB supports geo-distributed configurations, allowing data to be stored in multiple geographic locations, optimizing access times for distributed users, and ensuring data locality compliance.

The database provides automated healing in the face of hardware or software failures. It automatically rebalances and redistributes data as nodes are added or removed. CockroachDB is designed with cloud applications in mind, offering easy deployment in cloud environments, including [[Kubernetes]] integration.

It has built-in security features such as encryption at rest and in transit, along with strong access controls. CockroachDB is available as an open-source solution, with a commercial version offering additional features like enterprise-grade support and enhanced database management tools.

CockroachDB is wire-compatible with [[PostgreSQL]], meaning that applications built for PostgreSQL can often switch to CockroachDB without significant changes.
