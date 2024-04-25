Remote Procedure Call (RPC) is a protocol that one program can use to request a service from a program located on another computer in a network. RPC is used for communication between processes, typically across different machines. The main idea of RPC is to make a remote function call, which appears similar to a local function call, abstracting the details of network communication.

RPC abstracts the complexity of network communication so that developers can focus on the logic rather than the details of the network operations. To the developer, the remote procedure call looks and behaves like a local procedure call.

RPC typically follows a [[Client-Server Architecture|client-server]] model. The client sends a request to the server to execute a procedure, and the server returns the results of the executed procedure to the client.

In RPC, 'stubs' are used on both the client and server sides. The client-side stub acts as if it were the server, receiving the calls, arguments, and handling the process of sending them to the server. The server-side stub receives this information, executes the procedure, and sends back the results.

RPC involves marshalling (packing) parameters into a message format and unmarshalling (unpacking) them on the receiving side. This is necessary because the client and server might be using different architectures and data representations.

RPC can be synchronous or asynchronous. In synchronous RPC, the client waits for the server to finish processing the call before continuing its execution. In asynchronous RPC, the client proceeds without waiting for the server response.

RPC can be implemented over various transport protocols, such as [[TCP-IP|TCP/IP]] or [[User Datagram Protocol|UDP]], depending on the requirements like reliability and speed. Some RPC systems use an Interface Definition Language (IDL) to define the interface between the client and the server.

RPC is used in distributed computing environments, client-server architectures, microservices architectures, and cloud computing services.

There are various implementations and variants of RPC, including [[XML-RPC]] (where the procedure calls are made using [[Extensible Markup Language|XML]]), [[JSON-RPC]] (using [[JavaScript Object Notation|JSON]]), and gRPC (developed by Google, using Protocol Buffers and HTTP/2).

Security is an important aspect of RPC, as data is transferred over networks. Implementations often include authentication, encryption, and other security mechanisms.