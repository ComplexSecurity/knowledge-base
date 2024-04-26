In [ASP.NET](../frameworks/aspnet.md), `Response.WriteFile()` is a method of the `HttpResponse` class, used to write the contents of a file directly to the HTTP response output stream. This method is particularly useful when you want to serve files from your server to the client, such as downloading a file or displaying an image.

It reads the contents of a specified file and writes them directly to the HTTP response. This is done without loading the entire file into memory, which is efficient for large files. Often used in conjunction with setting the `ContentType` property of the `HttpResponse` object, to inform the browser about the type of content being sent.

Commonly used for implementing file download functionality in ASP.NET applications. By setting appropriate headers, you can prompt the user to download the file instead of displaying it.

The syntax is:

```csharp
Response.WriteFile(string path);
```

- `path`: The path of the file to be written to the response.

An example usage may be serving an image:

```cs
Response.ContentType = "image/jpeg";
Response.WriteFile("/path/to/image.jpg");
```

Or even prompting a file download:

```cs
Response.ContentType = "application/octet-stream";
Response.AppendHeader("Content-Disposition", "attachment; filename=example.txt");
Response.WriteFile("/path/to/example.txt");
Response.End();
```

!!! info
    In the download example, `ContentType` is set to a general binary (`application/octet-stream`), and the `Content-Disposition` header is used to prompt the browser to download the file, rather than attempting to display it.

The `Response.WriteFile()` function in ASP.NET itself is not inherently vulnerable, but its usage can lead to security vulnerabilities, especially if user input is used to determine the file path without proper validation. The primary concern in such scenarios is a security vulnerability known as Path Traversal or [Directory Traversal](../security/dirtrav.md).

Consider an ASP.NET web application where a user can request to view a file, and the file path is taken directly from the user input:

```csharp
public void ProcessRequest(HttpContext context)
{
    string filePath = context.Request.QueryString["file"];
    
    // Vulnerable usage of Response.WriteFile
    context.Response.ContentType = "application/octet-stream";
    context.Response.WriteFile(filePath);
    context.Response.End();
}
```

!!! danger
    In this example, an attacker could manipulate the file path to access sensitive files. For instance, if the application is hosted at `http://example.com`, an attacker might access:

```http
http://example.com?file=../../web.config
```

This URL could potentially give the attacker access to the `web.config` file, a critical configuration file in ASP.NET applications.

