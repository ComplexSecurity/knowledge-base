JavaDoc is a documentation generator tool for the [[Java]] programming language provided by Oracle. It is used for generating API documentation in [[HTML]] format from Java source code, based on the JavaDoc comments. These comments are specially formatted multi-line comments that precede class, method, and field declarations.

JavaDoc provides a standard format for documenting Java classes, interfaces, methods, variables, and packages. It generates HTML documentation from the source code, making it easy to browse and read. JavaDoc uses annotations (starting with `/**` and ending with `*/`) to identify documentation comments.

Within these comments, tags such as `@param`, `@return`, `@throws`, `@see`, and `@author` provide additional information and structure.

It is primarily used to document the public API of a Java class. This is crucial for both internal and external developers who use or maintain the code. JavaDoc comments are placed directly in the source code, making it easier to keep the documentation up-to-date with the code. IDEs like Eclipse or IntelliJ IDEA use JavaDoc comments to provide contextual help and documentation while coding.

An example includes:

```java
/**
 * This class represents a simple example.
 * @author John Doe
 */
public class Example {

    /**
     * Adds two integers.
     * @param a the first integer
     * @param b the second integer
     * @return the sum of a and b
     */
    public int add(int a, int b) {
        return a + b;
    }
}
```


!!! info
    The `Example` class and its method `add` have JavaDoc comments describing their purpose, parameters, and return values.

JavaDoc is typically run from the command line or through an IDE. The JavaDoc tool processes the source files and generates [[HTML]] files that can be hosted or distributed for reference.

