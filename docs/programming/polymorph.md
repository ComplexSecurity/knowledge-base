Polymorphism is a fundamental concept in [Object-Oriented Programming](../programming/oop.md) that refers to the ability of different objects to respond in their own way to the same message (or method call). The term originates from Greek, meaning "many forms." In programming, it allows objects of different classes to be treated as objects of a common superclass.

There are types of Polymorphism:

1. **Compile-Time Polymorphism (Static Polymorphism)**: This is achieved through method overloading or operator overloading. Here, the response to a function is determined at compile time. In languages like [C++](../programming/cpp.md), for instance, you can have multiple functions with the same name but different parameters.
2. **Run-Time Polymorphism (Dynamic Polymorphism)**: This is mainly achieved through method overriding, where a method in a subclass has the same name and signature as a method in its superclass. The specific version of the method that gets executed is determined at runtime, based on the type of the object that invokes the method.

Consider a class `Animal` with a method `makeSound()`. There are also two subclasses, `Dog` and `Cat`, each with their own implementation of `makeSound()`.

```java
class Animal {
    void makeSound() {
        System.out.println("Some sound");
    }
}

class Dog extends Animal {
    void makeSound() {
        System.out.println("Bark");
    }
}

class Cat extends Animal {
    void makeSound() {
        System.out.println("Meow");
    }
}

public class TestPolymorphism {
    public static void main(String args[]) {
        Animal a;
        a = new Dog();
        a.makeSound(); // Prints "Bark"

        a = new Cat();
        a.makeSound(); // Prints "Meow"
    }
}
```

In this [Java](../programming/java.md) example, `Animal` is the superclass, and `Dog` and `Cat` are subclasses. Each class has its own implementation of `makeSound()`. The type of object (`Dog` or `Cat`) determines which `makeSound()` method is called at runtime.

Polymorphism allows for writing flexible and scalable code as you can write code that works on the superclass level but can work with any subclass. This means new subclasses can be introduced with little to no modification to existing code. It supports the use of inheritance, allowing for the reuse of code and reduction of redundancy.

