External XML entities in the context of [[Extensible Markup Language|XML]] and web security are a type of XML entity that references content external to the XML document itself. In XML, entities are a way of representing certain items, typically as a reference to include content. External entities can be used to include external content in an XML document, but they can also pose significant security risks if not handled properly.

An external XML entity is defined in a [[Document Type Definition (DTD)]] or in an XML schema and typically references content from an external source, like a file on the server or a URL. When the XML parser processes the XML document, it can replace these external entity references with the actual content from the external source.

An external XML entity is usually declared in the DTD using something like:

```xml
<!ENTITY entity_name SYSTEM "external_resource">
```

Where `entity_name` is the name of the entity, and `external_resource` is the URI of the external content. In the XML document, these entities are referenced using the `&` symbol followed by the entity name; for example, `&entity_name;`.

External entities can be exploited in an [[XML External Entities (XXE)|XXE attack]]. If an attacker can insert or manipulate external entity references in an XML document and the XML parser processes these entities, it can lead to various security issues, such as:

- **Data Exfiltration**: Reading sensitive files from the server and sending the data out.
- [[Server-Side Request Forgery]] (SSRF): Making requests to internal systems that the server has access to.
- [[Denial of Service (DoS) Attacks|Denail of Service (DoS) Attacks]]: By referencing entities that lead to large amounts of data being processed or recursive entity loading.
