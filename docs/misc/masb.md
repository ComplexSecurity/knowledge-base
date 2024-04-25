  
Microsoft Azure Service Bus is a fully managed messaging service provided by Microsoft [[Azure]]. It enables communication between applications and services, both within the Azure cloud and on-premises. Azure Service Bus supports different messaging patterns, including publish/subscribe, point-to-point, and request/response.

Messaging Patterns:

- **Publish/Subscribe (Topics and Subscriptions)**: Azure Service Bus Topics allow publishers to send messages to a topic, and subscribers can receive messages from specific subscriptions within that topic. This pattern enables one-to-many communication.
- **Point-to-Point (Queues)**: Azure Service Bus Queues provide a one-to-one communication pattern. Messages sent to a queue are retrieved by a single receiver (consumer). This pattern ensures that each message is processed by only one consumer.

Azure Service Bus ensures reliable message delivery by supporting features such as message durability, retries, and dead-lettering. Messages are stored persistently, and consumers can retrieve them even after temporary failures.

Azure Service Bus supports message sessions, allowing related messages to be processed in a specific order. This is useful in scenarios where a group of related messages needs to be handled together. Messages can be automatically forwarded from one queue or topic/subscription to another. This feature is useful for routing messages to different destinations based on specific criteria.

Messages that cannot be processed successfully after a certain number of retries are moved to a dead-letter queue. This allows for further analysis and handling of failed messages. Azure Service Bus can be integrated with Azure Relay to enable secure and hybrid communication between on-premises applications and those hosted in Azure.

Topics and queues can be partitioned to improve scalability and throughput. Each partition operates independently, allowing for parallel processing of messages. Messages can be scheduled for future delivery, allowing for time-sensitive communication scenarios.

Azure Service Bus uses namespaces to group related messaging entities. Access control is managed through shared access policies, allowing fine-grained control over who can send or receive messages. A tool called Azure Service Bus Explorer provides a graphical user interface for managing and interacting with Azure Service Bus entities. It simplifies tasks such as creating queues, topics, and subscriptions.

Azure Service Bus provides SDKs and [[APIs]] for various programming languages, including [[Dotnet|.NET]], [[Java]], [[Python]], [[NodeJS|Node.js]], and more. This makes it easy for developers to integrate messaging capabilities into their applications.


