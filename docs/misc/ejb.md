Enterprise JavaBeans (EJB) is a server-side software component architecture used in [[Java]] Platform, Enterprise Edition (Java EE) for building robust, scalable, transactional, and multi-user secure enterprise-level applications. EJBs are used to encapsulate business logic, which can then be reused without the need for developers to handle complex aspects like transaction management, multi-threading, connection pooling, and other low-level functionalities.

Types of EJBs:

- **Session Beans**: Handle business logic. They come in two types:
  - **Stateless Session Beans**: Do not maintain client state across method calls.
  - **Stateful Session Beans**: Maintain client state across method calls.
- **Message-Driven Beans (MDBs)**: Used for handling asynchronous messages from a queue or topic.
- **Singleton Session Beans**: Similar to stateless session beans but there's only one instance for the entire application, useful for shared states.

EJBs run in an EJB container, which provides services like transaction management, security, remote access, concurrency control, and lifecycle management, relieving developers from handling these concerns explicitly.

EJBs support both declarative and programmatic transaction management, ensuring data consistency and integrity. The EJB container can manage security, providing declarative role-based access control.

EJBs can be accessed remotely or locally. Remote EJBs can be accessed by clients outside the EJB container, typically over a network, while local EJBs are accessed within the same application. While EJBs themselves are not responsible for data persistence, they can integrate with the [[Java Persistence API (JPA)]] for database access.

EJBs support interceptors to allow for cross-cutting concerns like logging or auditing. EJBs are registered and looked up in the [[JNDI]] directory, which is a part of the Java EE platform. EJBs promote a component-based development approach, where business logic is modularized and encapsulated in enterprise beans.

Despite their powerful features, EJBs have seen a decline in popularity due to their complexity and heavyweight nature. Modern Java EE and Jakarta EE platforms and frameworks like Spring and MicroProfile offer simpler and more flexible alternatives for many of the functionalities provided by EJBs.
