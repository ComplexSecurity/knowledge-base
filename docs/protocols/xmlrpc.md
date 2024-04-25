XML-RPC (XML Remote Procedure Call) is a protocol that uses [[Extensible Markup Language|XML]] to encode its calls and [[HTTP Protocol|HTTP]] as a transport mechanism. It's a simple way to execute functions or procedures on a remote server. In XML-RPC, a client sends an XML request to a server specifying the method to be invoked and the parameters to pass. The server then returns a response in XML format.

The client sends an XML document to the server with details of the method call. For example, an XML request to invoke a method `addNumbers` with two parameters might look like this:

```xml
<?xml version="1.0"?>
<methodCall>
    <methodName>addNumbers</methodName>
    <params>
        <param><value><int>5</int></value></param>
        <param><value><int>10</int></value></param>
    </params>
</methodCall>
```

The server processes the request, executes the specified method, and returns an XML response, such as:

```xml
<?xml version="1.0"?>
<methodResponse>
    <params>
        <param><value><int>15</int></value></param>
    </params>
</methodResponse>
```

This example demonstrates a basic XML-RPC interaction where the client requests the addition of two numbers, and the server responds with the result.
