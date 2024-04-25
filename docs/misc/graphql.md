GraphQL is a specification for how to talk to an [[APIs|API]]. It's typically used over [[HTTP Protocol|HTTP]] where the key idea is to POST a "query" to an HTTP endpoint, instead of hitting different HTTP endpoints for different resources.

GraphQL is designed for developers of web/mobile apps (HTTP clients) to be able to make API calls to fetch exactly the data they need from their backend APIs.

GraphQL is a query language and server-side runtime for APIs that prioritizes giving clients precisely the data they request and no more, unlike other API-building methods. For example, [[REST APIs|REST]] depends on endpoints, thus unable to fetch only the needed data.

![[graphql.png]]

Every GraphQL service defines a set of types that describe the possible data you can query on that service (that’s the schema). Then, when queries and mutations come in, they are validated and executed against that schema and processed using resolvers.

So a complete GraphQL implementation must have two parts: **schemas & resolvers**.

![[graphql2.png]]

A GraphQL operation can either be

- **Read** operation, known as **Query**, is used to read or fetch values
- **Write** operation, known as **Mutation**, is used to write or delete values.

In both cases, the operation is a simple string that a GraphQL server can parse and respond to with specifically formatted data. [[JavaScript Object Notation|JSON]] is usually the popular response format for mobile and web applications.