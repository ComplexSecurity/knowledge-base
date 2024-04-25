Contexts and Dependency Injection (CDI) is a set of services and [[APIs]] that brings the concept of dependency injection to [[Java Enterprise Edition (Java EE)|Java EE (Enterprise Edition)]]. It allows various components of a Java EE application, such as [[Enterprise JavaBeans (EJBs)|EJBs (Enterprise JavaBeans)]], [[Java Persistence API (JPA)|JPA (Java Persistence API)]] entities, and [[JSF]](JavaServer Faces) managed beans, to interact with each other in a more decoupled manner. CDI is a part of the Java EE platform, but it can also be used in Java SE applications.

CDI simplifies the process of connecting application components (beans), by allowing them to be injected at runtime, rather than being hard-coded or looked up manually. This makes the application easier to develop and maintain.

CDI uses a type-safe approach for dependency injection, minimizing runtime errors and improving code readability. CDI manages the lifecycle of beans with defined scopes, such as `RequestScoped`, `ApplicationScoped`, `SessionScoped`, and `ConversationScoped`. This helps in managing the state of beans according to the lifecycle of the application or its components.

CDI is designed to work seamlessly with various Java EE components, enhancing the capabilities of EJBs, JSF, JPA, and [[JAX-RS (Java API for RESTful Web Services)]]. CDI includes an event model that allows beans to produce and consume events, facilitating loose coupling and better separation of concerns.

It supports interceptors and decorators, which can be used to modify or extend the behavior of beans, for example, adding logging or security checks. CDI allows for the creation of portable extensions that can integrate with the container’s lifecycle, enabling customization and integration of third-party frameworks.

CDI integrates with the Unified EL, allowing CDI beans to be used directly in the JSF user interface and other EL contexts. For some use cases, CDI provides a lighter alternative to EJB, offering many of the same features without the need for a full EJB container.

CDI introduces the concept of stereotypes, which allow for encapsulating metadata about beans, making configuration more reusable and reducing boilerplate code.
