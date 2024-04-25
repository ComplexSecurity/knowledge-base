JSON-P, short for JSON Processing, refers to the [[Java]] API for processing JSON ([[JavaScript Object Notation]]) data. This API, also known as `javax.json`, provides a portable standard library for parsing, generating, transforming, and querying JSON data in Java. 

JSON-P is a part of the [[Java Enterprise Edition (Java EE)]], but it can also be used in Java Standard Edition (Java SE) applications.

JSON-P provides two models for processing JSON data:
- The Object Model, which is a high-level API and uses a DOM ([[Document Object Model]]) like approach.
- The Streaming Model, which is a low-level [[APIs|API]] and uses an event-driven approach.

The Object Model API creates an in-memory tree representation of the JSON data. It allows reading, transforming, and writing JSON data. The API is similar to [[Extensible Markup Language|XML]] processing APIs and is useful for scenarios where random access to the parsed JSON structure is required.

The Streaming API reads and writes JSON sequentially without loading the complete document into memory. This approach is more efficient in terms of memory usage and is faster for large JSON data sets.

JSON-P provides builders to create JSON objects and arrays from scratch. It also offers parsers to read JSON data from input sources and write JSON data to output sources. The API allows for the transformation of JSON data by adding, removing, and modifying elements of the JSON structure.

JSON-P doesn’t directly support querying JSON data. However, it can be used in conjunction with other libraries like JSON-Path for querying. JSON-P integrates well with other Java technologies, such as [[JAX-RS (Java API for RESTful Web Services)|JAX-RS]] for building [[REST APIs|RESTful]] web services that consume and produce JSON data.

As part of the Java EE platform, JSON-P provides a standardized way to handle JSON in Java, avoiding the need for third-party libraries. Being a standard Java API, JSON-P ensures portability across different Java environments.

JSON-P is suitable for applications that need to parse, generate, or transform JSON data, like RESTful services, applications communicating with [[Non-relational Database|NoSQL databases]], and more.
