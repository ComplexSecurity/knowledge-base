Universal Description, Discovery, and Integration (UDDI) is a platform-independent, open framework for describing services, discovering businesses, and integrating business services using the Internet. UDDI is an [XML](../programming/xml.md)-based standard for distributing information about web services and enabling businesses to find and communicate with each other.

UDDI can be thought of as a directory service for web services, where businesses can publish information about their services and search for other businesses' services.

UDDI specifications include three main parts

- **White Pages**: Contain general information about the service provider, such as the company name, address, contact details, etc.
- **Yellow Pages**: Organize services into categories, based on standard taxonomies.
- **Green Pages**: Provide technical information about the services offered, including references to the actual services and their specifications (like [WSDL](../misc/wsdl.md) documents).

UDDI enables service consumers to discover web services that meet certain criteria, supporting the dynamic discovery of service endpoints and service descriptions. At its core, UDDI is a registry for businesses and their services, enabling businesses to list themselves on the Internet, similar to a digital 'phone book' of web services.

UDDI uses [SOAP](../misc/soap.md) (Simple Object Access Protocol) for communication, and services are typically described using WSDL (Web Services Description Language). It was designed to promote the integration of electronic business services and to facilitate interoperable and platform-independent web services.

Initially, UDDI was anticipated as a crucial component of web services infrastructure. However, its adoption has been limited, and its importance has declined with the rise of other service discovery and integration methods.

While public UDDI registries have not been widely adopted, the concept and technology are used in private registries within organizations and enterprises. UDDI was intended to play a significant role in [Service-Oriented Architecture (SOA)](../misc/soa.md) by enabling dynamic binding of services, though in practice, many SOA implementations do not rely on it.

UDDI has been criticized for its complexity and for not being as dynamic as originally envisioned. In many modern service architectures, simpler and more flexible discovery mechanisms are often preferred.
