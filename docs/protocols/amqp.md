The Advanced Message Queuing Protocol (AMQP) is an open standard protocol for message-oriented middleware. The primary goal of AMQP is to enable interoperability among various message systems and applications. It provides a platform-independent method to ensure messages are safely and efficiently transferred between systems, making it a popular choice for enterprise messaging solutions.

AMQP is used in message-oriented middleware, allowing systems to communicate via messages in a reliable and scalable way. It’s designed to facilitate complex messaging scenarios between distributed and diverse systems.

Unlike protocols like [[HTTP Protocol|HTTP]] or [[Simple Mail Transfer Protocol|SMTP]], which are text-based, AMQP is a binary protocol. This makes it more efficient for network transmission and better suited for high-volume messaging. A key feature of AMQP is its emphasis on interoperability, enabling different software systems, possibly implemented in different programming languages on different platforms, to communicate.

AMQP provides various features to ensure reliable message delivery, including message acknowledgment, durable subscriptions, and transactions. It also supports secure communications through [[SSL-TLS|SSL/TLS]].

AMQP enables various patterns of communication, including point-to-point, publish-subscribe, and request-response. It allows messages to be queued, stored, and forwarded, handling complex routing scenarios. AMQP uses the concept of exchanges and bindings to route messages to the correct queues based on attributes like routing keys or headers.

AMQP 1.0, the version standardized by OASIS (Organization for the Advancement of Structured Information Standards), focuses on the message-oriented model and is not backward compatible with earlier, broker-centric versions (0-9-1, 0-10).

It’s widely used in financial services, telecommunications, and other industries where robust messaging systems are critical. Several open-source and commercial AMQP implementations exist, such as [[Apache Qpid]], [[RabbitMQ]], and [[Microsoft Azure Service Bus]].

While similar to other messaging protocols like [[MQTT]] or [[JMS]], AMQP is distinguished by its binary nature, interoperability, and reliability features.

