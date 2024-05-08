[Serialization](../misc/serial.md) is the process of turning some object into a data format that can be restored later. People often serialize objects in order to save them for storage, or to send as part of communications.

**Deserialization** is the reverse of that process, taking data structured in some format, and rebuilding it into an object. Today, the most popular data format for serializing data is [JSON](../misc/json.md). Before that, it was [XML](../programming/xml.md).

However, many programming languages have native ways to serialize objects. These native formats usually offer more features than JSON or XML, including customizability of the serialization process.

Unfortunately, the features of these native deserialization mechanisms can sometimes be repurposed for malicious effect when operating on untrusted data. Attacks against deserializers have been found to allow denial-of-service, access control, or [Remote Code Execution](../security/rce.md) (RCE) attacks.
