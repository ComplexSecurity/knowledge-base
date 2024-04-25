XInclude (XML Inclusions) is a part of the [[Extensible Markup Language|XML]] specification that defines a standard way to include external or internal content into an XML document. XInclude provides a mechanism for merging XML documents, or parts of documents, into a single composite document. This is particularly useful in situations where you want to assemble XML data from various sources or modularize XML documents.

XInclude uses special XML elements to specify what content should be included and where. The most commonly used element is `<xi:include>`, which has attributes to specify the source of the content:

- `href`: The URI of the document to include. This can be a local file or a URL.
- `parse`: This attribute determines how the included content should be parsed. It can be set to "xml" if the content is XML or "text" for plain text.
- `xpointer`: (optional) An [[XPointer]] expression that specifies a fragment of the document to include, allowing for partial document inclusion.

A simple example could be:

```xml
<document>
  <title>My Composite Document</title>
  <content>
    <xi:include href="content_section.xml" parse="xml" xmlns:xi="http://www.w3.org/2001/XInclude"/>
  </content>
</document>
```

In this example, the `<xi:include>` element is used to include the content of `content_section.xml` into the main document.

XInclude can be exploited in [[XML External Entities (XXE)]] attacks, where an attacker could reference external entities or sensitive files in the `href` attribute. If the XML parser processes these inclusions, it could lead to data exposure, data exfiltration, or service disruption.
