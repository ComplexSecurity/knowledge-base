Remote Method Invocation (RMI) is a [[Java]] API that allows an object running in one [[Java Virtual Machine (JVM)]] to invoke methods on an object running in another JVM. RMI is used primarily for building distributed applications, enabling objects to communicate directly across a network in a way that is largely indistinguishable from method calls on local objects.

RMI allows a Java object located on one machine (the client) to invoke methods on an object (the server) located on another machine, as if the object were located on the client machine. It is used for distributed computing, where processing power and resources are spread across different networked computers.

The architecture of RMI includes the client, the server, and the RMI registry. The registry is used for locating the remote objects. Each remote object is registered with the RMI registry using a unique name.

In RMI, a 'stub' object on the client side represents the remote object. When a method is invoked on the stub, it forwards the request to the remote 'skeleton' object on the server side, which then invokes the method on the actual remote object. In more recent versions of Java (since Java 2), the skeleton is no longer used, but the term is sometimes still used to describe server-side RMI operations.

RMI uses Java serialization to marshal and unmarshal parameters. The objects passed between the client and server must implement the `Serializable` interface. The RMI registry is a simple server-side naming service that allows clients to get a reference (stub) to a remote object.

RMI includes support for [[SSL-TLS|SSL/TLS]] and can be configured to authenticate and encrypt RMI traffic. While RMI can be used in standalone applications, it also forms the basis for higher-level services provided in Java EE, such as [[Enterprise JavaBeans (EJBs)|Enterprise JavaBeans (EJB)]]. Methods invoked via RMI can throw `RemoteException` to indicate communication-related errors during the execution of a remote method call.

RMI is suitable for distributed applications like remote monitoring and management systems, distributed data processing, and client-server applications where Java is the primary language.
