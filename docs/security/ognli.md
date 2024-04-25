OGNL ([[Object Graph Navigation Language]]) injection is a security vulnerability that occurs when an application allows unsanitized user input to be evaluated as OGNL expressions. OGNL is a powerful expression language used in various [[Java]] frameworks, such as [[Apache Struts 2|Apache Struts 2]], to navigate and manipulate object graphs.

OGNL is primarily used for expressing expressions that navigate and manipulate object graphs. It allows users to access and modify properties of Java objects. OGNL injection arises when an application doesn't properly validate and [[Input Sanitization|sanitize user input]] before interpreting it as OGNL expressions. Attackers can manipulate input fields to inject malicious OGNL expressions, leading to unauthorized access, data manipulation, or [[Knowledge Base/Remote Code Execution]].

OGNL injection is often associated with web applications that use Java frameworks like Apache Struts 2. Attackers may craft malicious input to exploit vulnerabilities in the application's handling of OGNL expressions.

To prevent OGNL injection, developers should validate and sanitize user input before using it in OGNL expressions. Input validation, proper encoding, and the use of [[parameterized queries]] or prepared statements are essential measures to protect against this type of injection.

Consider a web app using Apache Struts 2 with the following action:

```java
public class UserAction extends ActionSupport {
    private String username;

    // Getter and setter for username

    public String execute() {
        // Process user input
        return SUCCESS;
    }
}
```

If the application uses user input directly in OGNL expressions without proper validation, an attacker could manipulate the username parameter to inject malicious OGNL expressions:

```perl
http://example.com/user.action?username=%{%23a%3d(new%20java.lang.ProcessBuilder(new%20java.lang.String[]{'command','arg1'})).start(),%23b%3d%23a.getInputStream(),%23c%3dnew%20java.io.InputStreamReader(%23b),%23d%3dnew%20java.io.BufferedReader(%23c),%23e%3dnew%20char[50000],%23d.read(%23e),%23f%3d%23e,%23fos%3dnew%20java.io.FileOutputStream(%23f),%23fos.close()}"
```

In this example, the attacker attempts to execute arbitrary commands on the server by injecting a malicious OGNL expression.