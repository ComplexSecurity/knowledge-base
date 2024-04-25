Java Message Service (JMS) is a [[Java]] [[APIs|API]] that allows applications to create, send, receive, and read messages. Designed by Sun Microsystems, JMS is a part of the [[Java Enterprise Edition (Java EE)]] and provides a standard way for Java applications to access messaging systems and perform asynchronous communication. It's widely used in enterprise application integration and supports various messaging patterns, primarily point-to-point and publish-subscribe models.

JMS is used for communication between different parts of a distributed application. It allows loose coupling, reliability, and asynchronous communication between different components of the application.

In this model, messages are sent to a specific queue and are consumed by one receiver. This is typically used for scenarios where a message must be processed by only one consumer. In the publish-subscribe model, messages are published to a topic. Multiple consumers can subscribe to the topic and receive messages. This is suitable for broadcasting information to multiple receivers.

JMS enables asynchronous communication, which means the message sender does not need to wait for a response and can continue processing. The receiver can process the message and respond at its own pace.

JMS is an API and requires a messaging system implementation, known as a JMS provider, to function. Examples include [[Apache ActiveMQ]], [[IBM MQ]], and [[Oracle WebLogic]] JMS. JMS supports various message types, including simple text messages, object messages (serialized Java objects), bytes messages (for byte streams), map messages (key-value pairs), and stream messages (a stream of primitive values).

JMS provides different levels of reliability and quality of service, including guaranteed delivery, duplicate prevention, and message persistence. JMS is often used in conjunction with other Java EE technologies, like [[Enterprise JavaBeans (EJBs)]], [[Java Persistence API (JPA)]], and [[Java Transaction API (JTA)]].

JMS is commonly used in enterprise applications for scenarios like inventory management, order processing systems, and inter-service communication. A JMS client is a Java application or component that produces and/or consumes messages.