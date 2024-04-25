SGML, or Standard Generalized Markup Language, is a standard for defining generalized markup languages for documents. ISO 8879, which was first published in 1986, defines SGML. It's a meta-language in which one can define markup languages for documents. SGML is not a document language in itself but a description of how to specify document languages.

SGML allows users to define their own markup languages for specific document types. This flexibility makes it suitable for a wide range of applications in different industries. SGML focuses on describing the structure and content of a document rather than its presentation. This approach separates the content from the formatting, enabling the same document to be presented in various ways.

SGML is best known as the parent language of [[HTML]] (HyperText Markup Language) and XML ([[eXtensible Markup Language]]). Both HTML and XML are derived from SGML, inheriting its principles of markup and structure definition.

SGML has been widely used in industries for technical documentation, where maintaining document structure and consistency is crucial. It's used in publishing for encoding and exchanging documents, especially where different document types and complex structures are involved. SGML has been used by government agencies and in defense systems for documentation purposes, given its ability to handle complex and structured documents.

With the rise of the web, HTML (a simpler SGML application) and later XML became more popular for many of the purposes SGML was used for. XML offers many of the same advantages as SGML but in a simpler format, making it more suitable for web applications. However, SGML's legacy lives on through XML and HTML, which continue to play a fundamental role in the structure of the web and data interchange.

First, an SGML declaration defines the rules for the markup language. Then, a [[Document Type Definition (DTD)]] specifies the structure of a particular type of document. Here's a hypothetical example:
#### SGML Declaration
This part is often predefined and specifies the syntax rules for the SGML application.

```xml
<!SGML "ISO 8879-1986">
```
#### Document Type Definition (DTD)
Suppose we are defining a simple article type:

```xml
<!DOCTYPE article [
<!ELEMENT article (title, body)>
<!ELEMENT title (#PCDATA)>
<!ELEMENT body (p+)>
<!ELEMENT p (#PCDATA)>
]>
```

In this DTD:

- `article` is the root element, containing `title` and `body`.
- `title` contains parsed character data (`#PCDATA`).
- `body` consists of one or more paragraphs (`p`).
- `p` represents a paragraph.
#### SGML Document Example
Based on the above DTD, an SGML document might look like this:

```xml
<article>
    <title>Example Article</title>
    <body>
        <p>This is the first paragraph of the example article.</p>
        <p>This is the second paragraph.</p>
    </body>
</article>
```

SGML itself is rarely used directly for documents; instead, it defines the rules for markup languages. The most famous application of SGML is HTML. SGML is highly flexible and can be used to define markup languages with complex structures, suitable for various industries and applications. The syntax and structure can become quite complex, especially for large DTDs in professional environments.