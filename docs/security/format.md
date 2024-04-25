Format string vulnerabilities are a class of security flaws commonly found in [[C]] or [[C++]] programs that occur when a program uses input data as a format string for output functions without proper validation or sanitization. This can lead to various types of attacks, including reading from or writing to arbitrary memory locations, which might result in unauthorized access, information disclosure, or crashes.

The vulnerability arises in functions like [[printf]], [[sprintf]], [[fprintf]], and similar functions in C/C++, which use format strings to determine how to interpret and display data. If an attacker can control the format string, they can manipulate these functions to execute harmful actions.

Consider a C program using `printf` function:

```c
char user_input[100];
scanf("%s", user_input);
printf(user_input); // Vulnerable
```

In this example, the program reads user input into a variable and then directly passes it to the `printf` function. If the user input contains format specifiers (like `%s`, `%x`, `%n`), they will be interpreted by `printf`, causing unintended behavior.

An attacker could use format specifiers to read memory locations adjacent to the format string. For example, inputting `%x %x %x` might print out memory contents. The `%n` specifier writes the number of characters printed so far to a provided memory address. An attacker could use this to write arbitrary values to arbitrary memory locations.

Incorrect format strings can lead to segmentation faults or crashes, potentially part of a [[Denial of Service (DoS) Attacks|denial-of-service]] attack.