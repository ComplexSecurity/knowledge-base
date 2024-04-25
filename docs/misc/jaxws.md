Java API for XML-Based Web Services (JAX-WS) is a set of APIs for building web services in [[Java]] using XML. It is part of the [[Java Enterprise Edition (Java EE)|Java EE (Enterprise Edition)]] platform and provides a standard way to develop [[SOAP]] (Simple Object Access Protocol) web services.

JAX-WS uses annotations to simplify the development of web services. Annotations are used to define the web service, its operations, and other aspects of the service. This reduces the amount of boilerplate code that developers need to write.

JAX-WS relies on [[WSDL]] for describing the contract of the web service. WSDL is an [[Extensible Markup Language|XML]]-based language that defines the operations, input and output parameters, and communication details of a web service. JAX-WS generates WSDL automatically based on the annotated Java code.

In JAX-WS, an endpoint is a Java class that contains methods annotated with `@WebMethod`. These methods represent the operations of the web service. The endpoint class is responsible for processing incoming requests and generating responses.

JAX-WS provides client APIs for consuming SOAP web services. Clients can be generated dynamically or using tools like `wsimport` that generate client code based on the WSDL contract. JAX-WS supports SOAP as the messaging protocol for web services. SOAP is a protocol for exchanging structured information in web services and is based on XML.

Handlers in JAX-WS allow developers to intercept the processing of inbound and outbound messages. Handlers can be used for tasks such as logging, security, or custom message processing. JAX-WS supports [[MTOM]] for efficient transmission of binary data in SOAP messages. MTOM allows large binary data, such as images or documents, to be transmitted as optimized binary attachments.

JAX-WS supports asynchronous web services, allowing clients to send requests asynchronously and receive responses at a later time.

A simple example of a JAX-WS annotated endpoint:

```java
import javax.jws.WebMethod;
import javax.jws.WebService;

@WebService
public class MyWebService {

    @WebMethod
    public String sayHello(String name) {
        return "Hello, " + name + "!";
    }
}
```

The `MyWebService` class is a JAX-WS endpoint with a single method (`sayHello`) that is exposed as a web service operation. The `@WebService` and `@WebMethod` annotations define the web service and its operations.


