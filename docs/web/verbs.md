The [[HTTP Protocol]] includes a collection of methods that are used to interact with server-side resources. There are commonly referred to as _HTTP request methods_ or _HTTP verbs_ and are intended to cover all possible types of interaction with resources.

While HTTP Request Methods typically perform different operations, there is an overlap in functionality, and depending on the task, several HTTP requests will have to be made before it is complete. There are also HTTP method properties to consider, including whether a HTTP request is safe, idempotent, or cacheable.

Some of the most commonly used HTTP Request Methods include:

| Method  | Description                                                                                                |
| ------- | ---------------------------------------------------------------------------------------------------------- |
| GET     | Requests a specific resource. Additional data can be passed via query strings in the URL                   |
| POST    | Sends data to the server. Handle many types of input. Data appended in request body after [[HTTP Headers]] |
| HEAD    | Requests headers returned from a GET request                                                               |
| PUT     | Create new resources on the server                                                                         |
| DELETE  | Deletes an existing resource on the server                                                                 |
| OPTIONS | Returns information about the server, such as methods accepted                                             |
| PATCH   | Applies partial modifications to the resource specified                                                    |


