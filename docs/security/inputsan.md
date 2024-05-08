Input sanitization in web applications refers to the process of cleaning and validating user input to ensure it is safe and appropriate before processing it or incorporating it into output. This is a critical security measure to prevent malicious inputs that could lead to vulnerabilities like [SQL Injection](), [Cross-Site Scripting]() (XSS), and other types of attacks.

Some key aspects of input sanitization include:

- **Validation** - involves checking if the input meets certain criteria before it is accepted. For example, ensuring an email address is in the correct format or a phone number only containing digits.
- Filtering - removing or replacing unwanted characters from the input. For example, stripping out script tags from text inputs to prevent XSS attacks.
- Escaping - in contexts where input is inserted into another language or system (like [Structured Query Language|SQL](), [HTML]() or [JavaScript]()), escaping involves modifying the input so that it is treated as data rather than code.
- Canonicalization - transforming input to a standardized or simplified form as attackers might use complex or encoded input to bypass simpler formats.
- Limiting input size - setting a max size for inputs can prevent [Buffer Overflows|buffer overflows]() and reduce the risk of [Denial of Service (DoS) Attacks|Denial of Service]() (DoS) attacks.