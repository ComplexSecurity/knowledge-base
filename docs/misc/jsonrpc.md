JSON-RPC is a remote procedure call protocol encoded in [[JavaScript Object Notation|JSON]]. It allows for sending messages, formatted as JSON, to a server that implements the JSON-RPC protocol. The server processes the request and returns a response, also in JSON format. This protocol is lightweight and stateless, making it suitable for various environments and applications, including [[web services]] and internal communications in distributed systems.

A client can send a JSON object to request a specific method execution. For example:

```json
{
  "jsonrpc": "2.0",
  "method": "addNumbers",
  "params": [5, 10],
  "id": 1
}
```

This request is asking to execute the `addNumbers` method with two parameters (5 and 10). The server, upon successfully executing the method, might respond with:

```json
{
  "jsonrpc": "2.0",
  "result": 15,
  "id": 1
}
```

This response indicates the result of the operation and correlates to the original request via the "id" field.

JSON-RPC's simple and lightweight structure makes it a popular choice for internal [[APIs]] and services where extensive data modeling is not required. It is particularly useful in environments where bandwidth and performance are considerations.

