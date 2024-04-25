Object-oriented programming (OOP) is a programming paradigm based on the concept of "objects," which can contain data and code: data in the form of fields (often known as attributes or properties), and code, in the form of procedures (often known as methods). OOP is a fundamental concept in modern software development, offering a structured approach to designing and building applications.

In OOP, objects are instances of classes, which define the properties and behaviors that the objects can have. Classes serve as blueprints for creating objects.

This principle involves bundling the data (attributes) and the methods (functions or procedures) that operate on the data into a single unit (class). It also involves restricting direct access to some of an object's components, which is a means of preventing accidental interference and misuse of the methods and data.

OOP allows for the creation of complex systems where the specific details are hidden and only the necessary aspects are presented. This simplifies programming and increases efficiency.

Classes can inherit properties and methods from other classes. A class that inherits from another class is typically called a subclass or derived class, and the class it inherits from is called the superclass or base class. Inheritance promotes code reuse and can lead to an efficient hierarchical structuring of code.

Polymorphism allows objects of different classes to be treated as objects of a common super class. The most common use of polymorphism is when a parent class reference is used to refer to a child class object.

OOP inherently promotes modularity, where applications can be broken down into smaller, manageable, and modular components (classes), which can be developed, tested, and maintained more easily.

Thanks to inheritance and polymorphism, OOP enables code reusability, which reduces redundancy and increases the efficiency of the development process.

Many modern programming languages support OOP principles, including [[Java]], [[CSharp|C#]], [[C++]], [[Python]], [[Ruby]], and [[PHP]].

Some examples include classes:

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model
```

Think of a class as a blueprint for a house. It defines the structure and capabilities, but is not a house itself.

Objects are also used:

```python
my_car = Car("Toyota", "Corolla")
```

An object is a specific instance of a class. Using the house analogy, if a class is the blueprint, an object is a house built from that blueprint. 

The next concept is Inheritance:

```python
class ElectricCar(Car):  # Inherits from Car class
    def __init__(self, make, model, battery_capacity):
        super().__init__(make, model)
        self.battery_capacity = battery_capacity
```

Inheritance allows a new class to extend an existing class. The new class inherits the attributes and methods of the existing class. As above, ElectricCar is now a type of "Car" but with additional attributes and potentially new methods specific to electric cars.

Polymorphism allows methods to do different things based on the object it is acting upon:

```python
class Animal:
    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return "Woof!"

class Cat(Animal):
    def speak(self):
        return "Meow!"
```

Both "Dog" and "Cat" override the "speak" method from "Animal" providing their unique implementations.

Finally, encapsulation involves bundling of data (attributes) and methods that operate on the data into a single unit or class and restricting access to some of the object's components:

```python
class BankAccount:
    def __init__(self):
        self.__balance = 0  # Private attribute

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount

    def get_balance(self):
        return self.__balance
```

Here, **\_\_balance** is a private attribute. It can't be accessed directly from outside the class, thus encapsulating and protecting it from unintended interference.