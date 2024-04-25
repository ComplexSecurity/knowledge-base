REST stands for **Representational State Transfer**. This means that when a [[client]] requests a resource using a REST API, the [[server]] transfers back the current state of the resource in a standardized representation.

REST APIs work by fielding requests for a resource and returning all relevant information about the resource, translated into a format that clients can easily interpret (this format is determined by the API receiving requests). Clients can also modify items on the server and even add new items to the server through a REST API.

REST APIs must follow six requirements:

- **Client-Server Separation** - client sends request to server and server responds back. Servers cannot make requests and clients cannot respond
- **Uniform Interface** - all requests/responses must follow a common protocol. For most REST APIs, the common language is [[HTTP Protocol|HTTP]].

To use HTTP with a REST API, the client sends a request in a specific format:

```html
GET https://www.googleapis.com/youtube/v3/channels?part=contentDetails
```

It contains 2 pieces of information:

- GET is the [[HTTP Verbs|HTTP method]].
- https://www.googleapis.com/youtube/v3/channels?part=contentDetails is the [[Uniform Resource Locator|URL]]

!!! info
    URL is also called an endpoint as it is the location where the API interacts with the client.

After validating the request, the host returns info about the target resource - usually sent in [[JavaScript Object Notation|JSON]]. 

Continuing the requirements:

- **Stateless** - all calls must be stateless. Every interacting is independent and each request and response provides all info required to complete the interaction.
- **Layered System** - servers/layers in API requests are there to add security, handle and distribute traffic or assist with other functions. Messages between client and target should always be formatted and processed the same way.
- **Cacheable** - when a server sends its response to a client, the response should indicate whether the resource provided can be cached and for how long.
- **Code on Demand** - API can send computer code to client in its response.

!!! important
    If an API adheres to this set of rules, it is a RESTful API


