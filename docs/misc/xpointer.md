XPointer, which stands for [[Extensible Markup Language|XML]] Pointer Language, is a system for addressing parts of an XML document. It extends the functionality of [[XPath]], a language used to select nodes in an XML document, by allowing more complex addressing that can include ranges of text and points between characters. XPointer is part of the XML family of technologies and is defined by the World Wide Web Consortium (W3C).

XPointer allows for the identification of fragments within XML documents. It's used as a fragment identifier in a URI to point to specific parts of an XML document. While XPath is used for simple expressions to select nodes, XPointer can describe more specific locations in an XML document, such as ranges or specific points within the text.

XPointer supports different schemes, such as the `xmlns` scheme for namespace handling, the `element()` scheme for element addressing, and the `xpointer()` scheme which uses XPath expressions.

An XPointer expression could look like this:

```xml
http://example.com/document.xml#xpointer(id("Chapter2"))
```

In this example:

- The URI points to an XML document named `document.xml`.
- The XPointer expression `#xpointer(id("Chapter2"))` identifies a fragment in the XML document with an ID of `Chapter2`.

XPointer can be used in web applications for deep linking directly to parts of XML-based documents like [[XHTML]], SVG, or XML databases. It's useful in XML processing applications where addressing specific parts of documents is required.

The complexity of XPointer expressions can lead to potential performance issues if not properly implemented. Like with XPath, there is a potential for [[XML External Entities (XXE)|XXE]] vulnerabilities if XPointer is used with untrusted data in an XML context. Properly configuring XML parsers and validating input is crucial to mitigate this risk.
