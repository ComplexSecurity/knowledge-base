Entity reference loops occur when an entity in an [[Extensible Markup Language|XML]] document refers to itself directly or indirectly, creating an infinite loop. This issue arises in the context of XML entities, which are a way of defining shortcuts for larger blocks of text or external data. Entity reference loops are particularly relevant in the context of [[XML External Entities (XXE)|XML External Entity (XXE)]] attacks and can lead to [[Denial of Service (DoS) Attacks|denial of service (DoS)]] conditions.

In XML, you can define entities, which are placeholders for some content. When an XML processor encounters an entity, it replaces the entity with the content it represents. A loop occurs when the replacement text of an entity includes a reference to the same entity, either directly or through other entities.

A simple XML document with a [[Document Type Definition (DTD)]] that defines entities could be:

```xml
<!DOCTYPE root [
<!ENTITY loop "loop: &loop;">
]>
<root>&loop;</root>
```

In this example, the entity `loop` is defined to include a reference to itself. When the XML processor tries to expand `loop`, it finds that it needs to expand `loop` again, and this goes on indefinitely, potentially causing the processor to crash or hang.

In web applications, if an XML parser tries to process a document with an entity reference loop, it can consume excessive system resources, leading to a DoS condition. Attackers might exploit XXE vulnerabilities by crafting malicious XML input that includes entity reference loops, aiming to crash the server or service that processes the XML.
