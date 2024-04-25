A Document Type Definition (DTD) is a set of markup declarations that define a document type for an [[Standard Generalized Markup Language (SGML)|SGML]]-family markup language (such as [[HTML]] and [[Extensible Markup Language|XML]]). A DTD specifies the legal building blocks of an XML document. It defines the document structure with a list of legal elements and attributes.

A DTD defines elements, their composition, and their content model. For example, it specifies which elements are allowed, in what order, and what content they can contain. It also defines attributes for elements and constrains their possible values. DTD allows the definition of entities, which can be used to define shortcuts for complex or frequently used text.

In web applications, DTDs are commonly used in XML data interchange formats. They ensure that XML documents conform to a predefined structure and data types, which is critical for data integrity and successful data exchange. XML parsers can use a DTD to validate XML documents, ensuring they meet the structure and constraints defined in the DTD.

[[XML External Entities (XXE)|XXE]] vulnerabilities arise when an XML processor evaluates external entity references within an XML document. An attacker can exploit XXE vulnerabilities by including hostile content in an XML document, which can lead to unauthorized data disclosure, [[Denial of Service (DoS) Attacks|denial of service]], [[server-side request forgery]], and other security issues.

If an XML parser processes XML files with DTDs and allows the definition of external entities, an attacker could define an entity that accesses a file on the server or interacts with external systems. An example of an XXE attack via DTD:

```xml
<!DOCTYPE data [
<!ELEMENT data (#ANY)>
<!ENTITY xxe SYSTEM "file:///etc/passwd">]>
<data>&xxe;</data>
```

In this example, the DTD defines an external entity `xxe` that tries to read the content of `/etc/passwd` (a sensitive file on Unix-like systems).
