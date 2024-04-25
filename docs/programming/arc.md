Automatic Reference Counting (ARC) is a memory management feature of [Objective-C](../programming/objectc.md) and [Swift](../programming/swift.md), the programming languages used for developing applications on Apple's macOS and iOS platforms. Introduced with Objective-C 2.0 and fully embraced in Swift, ARC automates the process of memory management, reducing the complexity of manual memory management and minimizing memory leaks.

ARC automatically keeps track of the number of references to objects in memory. When an object's reference count drops to zero (meaning it's no longer referenced in the program), ARC automatically deallocates (frees) that object from memory.

Each time you create a new reference to an object (for example, by assigning it to a variable or passing it in a method), ARC increments its reference count. Conversely, when the reference is no longer needed (like when the variable goes out of scope), ARC decrements the reference count. When an object’s reference count reaches zero, indicating that it's no longer in use, ARC automatically deallocates the object, freeing up the memory it occupied.

By automatically managing object lifecycles, ARC significantly reduces the chances of memory leaks—a common problem in manual memory management. With ARC, developers don't need to write explicit memory management code (like `retain` and `release` in Objective-C), leading to cleaner and more maintainable code.

Before ARC, Objective-C used manual retain/release for memory management. ARC was introduced as an option in Objective-C to simplify this process. Swift was designed with ARC integrated from the start. It handles memory management automatically for Swift objects, though manual memory management is still required when interacting with C APIs or for certain advanced tasks.

In Swift, you simply create and use objects, and ARC takes care of the rest:

```swift
class MyClass {
    var property: String
    init(property: String) {
        self.property = property
        print("\(property) initialized")
    }
    deinit {
        print("\(property) deinitialized")
    }
}

var example: MyClass? = MyClass(property: "Example")
example = nil // ARC decrements the reference count, triggering deinitialization
```

!!! info
    In this Swift example, when `example` is set to `nil`, ARC deallocates the `MyClass` instance, and its `deinit` block is called.

ARC introduces the concept of strong and weak references to help manage memory, especially in situations where retaining cycles (two objects keeping each other alive) might occur. When dealing with Core Foundation objects in Objective-C, developers still need to manage memory manually, even with ARC enabled.
