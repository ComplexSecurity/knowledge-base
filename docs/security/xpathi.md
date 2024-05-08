XPath Injection is a type of cyber attack that targets web applications that use [Extensible Markup Language|XML]() data for input and output. It occurs when a website constructs [XPath]() queries from user-supplied data without proper validation or sanitization.

XPath (XML Path Language) is used to query XML documents, and manipulating XPath queries can lead to unauthorized access to data or other malicious activities.

XPath Injection is similar to [SQL Injection]() but specifically targets applications that use XPath. Attackers inject malicious XPath expressions into queries, exploiting poorly coded XML data processing.

By manipulating XPath queries, an attacker can potentially gain access to unauthorized XML data, retrieve hidden information, or in some cases, even modify the data if the application allows for it.

The vulnerability primarily arises from the application's failure to properly validate or sanitize user input before incorporating it into an XPath query. This oversight allows attackers to alter the intended XPath query.

An example of vulnerable code is:

```xml
String xpathQuery = "/users/user[username/text()='" + userInput + "']";
```

In this example, `userInput` is directly concatenated into the XPath query. If `userInput` includes malicious XPath code, it can alter the query's behavior.
