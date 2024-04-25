ReDoS stands for Regular Expression Denial of Service. It is a type of [[Denial of Service (DoS) Attacks|Denial of Service (DoS)]] attack that targets the improper implementation and handling of [[regular expressions]] in various software and applications. This vulnerability can be exploited to cause a program or service to become unresponsive or consume excessive amounts of resources, such as CPU or memory, thus rendering it unable to serve legitimate requests.

ReDoS attacks exploit the fact that certain regular expressions can cause extreme situations in terms of computational time or memory usage when processing specially crafted input strings. These are typically regular expressions that have nested quantifiers or are highly ambiguous.

An attacker crafts a specific input string that triggers the vulnerable regular expression to perform an excessive number of operations or backtrack steps. For example, a regular expression designed to validate email addresses might be forced into extensive backtracking by a specially crafted email string, causing the service to hang or slow down significantly.

The performance impact can be severe enough to cause the application or service to become unresponsive, leading to a denial of service for other users and processes. A common example of a potentially vulnerable regular expression pattern is one that uses multiple nested quantifiers, like:

```regex
(a+)+
```

This pattern can be exploited with an input string like `aaaaaaaaaaaaaaaaaaaaax`. The regular expression engine tries to match the pattern in many different ways due to the nested quantifiers, which can lead to a combinatorial explosion of possibilities, consuming significant processing time.

