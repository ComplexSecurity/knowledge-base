WSDL, or Web Services Description Language, is an [[Extensible Markup Language|XML]]-based language used for describing the functionality offered by a web service. It provides a machine-readable description of how the service can be called, what parameters it expects, and what data structures it returns.

WSDL is a key component in the web services stack and plays a critical role in [[SOAP]] (Simple Object Access Protocol) web services. WSDL is used to describe the details of a web service in a standard way. It defines how to access a web service and what operations it will perform.

WSDL documents are written in XML, which makes them both human-readable and machine-processable. Although WSDL can be used with any web service, it is most commonly associated with SOAP web services. It specifies the SOAP actions and the data encoding method for HTTP-based SOAP services.

A WSDL document typically contains definitions of:

- **Types**: Data types used by the web service.
- **Message**: Abstract, typed definitions of the data being communicated.
- **Operation**: An abstract description of an action supported by the service.
- **Port Type**: An abstract set of operations supported by one or more endpoints.
- **Binding**: A concrete protocol and data format specification for a particular port type.
- **Service**: A collection of related endpoints.

WSDL helps in automating the details of web service discovery and integration, allowing for easier interoperation between different systems and platforms. WSDL is often used in conjunction with [[Universal Description, Discovery, and Integration (UDDI)]], an XML-based standard for describing, publishing, and finding web services.

Many development tools can automatically generate client code (stubs) for calling a web service based on its WSDL description. While WSDL is commonly used with SOAP over [[HTTP Protocol|HTTP]], it also supports other underlying network protocols.

WSDL 2.0, an updated version, adds additional features and addresses some limitations of WSDL 1.1, though 1.1 remains widely used. WSDL has been criticized for its complexity, and in some modern web service applications, it has been supplanted by more lightweight alternatives such as [[REST APIs|RESTful]] services, which often use simpler description formats.
