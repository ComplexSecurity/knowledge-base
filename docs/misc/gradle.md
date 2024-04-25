"Gradle" is a powerful and flexible build automation tool that's used primarily for [[Java]] projects, but it also supports other programming languages like C/C++, [[Python]], and Swift. It combines the best features of [[Ant]] and [[Apache Maven|Maven]] and adds its own set of unique capabilities. 

Gradle is particularly known for its Groovy-based domain-specific language (DSL) for describing builds, which offers a more expressive and concise way to define custom build logic than [[Extensible Markup Language|XML]].

Gradle build scripts are written in Groovy, a dynamic, object-oriented programming language for the Java platform, which makes the build scripts more flexible and easier to write compared to XML-based scripts used in Maven.

Gradle features a daemon mode that makes builds much faster by reusing computations from previous builds. It also offers advanced caching and parallel execution strategies, resulting in significant performance improvements over other build tools.

Like Maven, Gradle uses a central repository to manage project dependencies. It can import dependencies from Maven and Ivy repositories and can also publish artifacts to these repositories.

Gradle allows for extensive customization to meet the specific needs of a project. It supports custom tasks and offers a rich API for extending the tool with custom plugins. Gradle is well-suited for managing multi-project builds, enabling modularization of large software projects with ease.

Gradle is the official build tool for Android, making it a standard choice for [[Android]] app development. It brings powerful features for building, testing, and deploying Android applications. Gradle provides an innovative feature called build scans, which offers insights into build processes for performance optimization and troubleshooting.

Gradle inherits the “convention over configuration” principle from Maven but provides greater flexibility to override the conventions.