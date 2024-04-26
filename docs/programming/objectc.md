Objective-C is a programming language primarily used for developing software for Apple's macOS and iOS operating systems. It was developed in the 1980s and combines [C](../programming/c.md) language efficiency with the object-oriented capabilities of [Smalltalk](../programming/small.md). Before the introduction of [Swift](../programming/swift.md) by Apple in 2014, Objective-C was the primary language used for developing applications in the Apple ecosystem.

Objective-C is an object-oriented language, which means it allows developers to define classes, create objects, and implement inheritance, encapsulation, and [Polymorphism](../programming/polymorph.md). As a superset of C, Objective-C includes all functionalities of C and adds object-oriented features. This means any valid C code is also valid in Objective-C.

The language supports dynamic typing, allowing the type of an object to be determined at runtime, which can enhance flexibility and extensibility. One of the unique aspects of Objective-C is its use of message passing for invoking methods, which is different from function calling in traditional C.

Before the introduction of [Automatic Reference Counting (ARC)](../programming/arc.md), Objective-C used a manual reference counting system, but it now largely automates memory management.

Objective-C was the main language used for developing applications for Apple's desktop and mobile operating systems until the introduction of Swift. These are key Apple frameworks for macOS and iOS development, respectively, and were traditionally based on Objective-C.

An example:

```C
#import <Foundation/Foundation.h>

@interface MyClass : NSObject
- (void)myMethod;
@end

@implementation MyClass
- (void)myMethod {
    NSLog(@"Hello, World!");
}
@end

int main() {
    MyClass *myObject = [[MyClass alloc] init];
    [myObject myMethod];
    return 0;
}
```

!!! info
    This simple example demonstrates a class definition, method implementation, and object creation in Objective-C.


