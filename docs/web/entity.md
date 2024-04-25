Parameter entities in [[Extensible Markup Language|XML]] are a special type of entity used within [[DTD (Document Type Definition)|Document Type Definitions (DTDs)]] to define reusable components. They are similar to general entities but are specifically designed for use within the DTD to define and structure the DTD itself. Parameter entities are not used directly in the XML document's body; rather, they are used to parameterize the DTD, making it more modular and easier to maintain.

Parameter entities are declared in a DTD using the following syntax:

```xml
<!ENTITY % entity_name "entity_value">
```

`%` indicates that it is a parameter entity, `entity_name` is the name of the entity, and `entity_value` is the value or content of the entity. Once declared, parameter entities are referenced within the DTD using the `%` symbol followed by the entity name and a semicolon (`;`). For example:

```xml
%entity_name;
```

As an example, suppose you have a set of elements that are reused across various element declarations. You can define a parameter entity for this set:

```xml
<!ENTITY % items "item1 | item2 | item3">
```

And use it in an element declaration like this:

```xml
<!ELEMENT myElement (%items;)>
```

Parameter entities can be used to include entire sections of a DTD, making it modular. For example:

```xml
<!ENTITY % section1 SYSTEM "section1.dtd">
<!ENTITY % section2 SYSTEM "section2.dtd">
```

Then, these sections can be included in the DTD:

```xml
%section1;
%section2;
```

Parameter entities, like other types of DTD entities, can be exploited in [[XML External Entities (XXE)|XML External Entity (XXE)]] attacks if an attacker can inject or alter DTDs in an XML document. This is particularly risky when the parameter entities reference external resources. To mitigate this, it's recommended to configure XML parsers to disable the processing of external entities and parameter entities from untrusted sources.

