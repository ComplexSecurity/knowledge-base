`fprintf` is a function in the [C](../programming/c.md) standard library used for formatted output to a stream. It is similar to [printf](../programming/printf.md), but instead of writing output to the standard output (typically the screen), `fprintf` writes the output to the specified file stream. The function prototype is:

```c
int fprintf(FILE *stream, const char *format, ...);
```

`fprintf` takes a file stream (like a file pointer returned by `fopen`) and a format string followed by an unspecified number of additional arguments. The vulnerabilities in `fprintf` are generally related to the format string. If an attacker can control the format string, they might exploit it in a way similar to [Format String Vulnerabilities](../security/format.md) in `printf`.

If the format string is not properly specified and user input is passed directly as a format string, it can lead to a format string vulnerability. An attacker might provide a format string that causes `fprintf` to perform unauthorized operations like reading from or writing to arbitrary memory locations. If `fprintf` is used to write more data to a buffer than it can hold, it can lead to buffer overflow vulnerabilities.

Consider a program that uses `fprintf` to write user input to a file:

```c
FILE *fp;
char user_input[100];

fp = fopen("log.txt", "w");
scanf("%99s", user_input);  // Read user input
fprintf(fp, user_input);   // Vulnerable
fclose(fp);
```

In this example, `user_input` is directly used in `fprintf` as a format string. An attacker could input a string like `%x %x %x` to potentially leak memory contents into the `log.txt` file. More maliciously, they could use `%n` to write values to memory, leading to code execution vulnerabilities.