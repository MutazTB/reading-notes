# Object Oriented Principles

The Object Oriented programming paradigm plays an important role in human computer interface.
It has different components that takes real world objects and performs actions on them, making live interactions between man and the machine.

This paradigm describes a real-life system where interactions are among real objects.

It models applications as a group of related objects that interact with each other.

The programming entity is modeled as a class that signifies the collection of related real world objects.

**components of object oriented programming.**
## 1. Inheritance

Inheritance allows us to define a class in terms of another class, which makes it easier to create and maintain an application. This also provides an opportunity to reuse the code functionality and speeds up implementation time.

When creating a class, instead of writing completely new data members and member functions, the programmer can designate that the new class should inherit the members of an existing class. This existing class is called the base class, and the new class is referred to as the derived class.

The idea of inheritance implements the IS-A relationship. 
For example, mammal IS A animal, dog IS-A mammal hence dog IS-A animal as well.

---

## 2. Polymorphism

polymorphism is often expressed as 'one interface, multiple functions'.

Polymorphism can be static or dynamic.
In static polymorphism, the response to a function is determined at the compile time. 
**C# provides two techniques to implement static polymorphism**
1. Function overloading
2. Operator overloading

In dynamic polymorphism, it is decided at run-time.

---

## **Abstract classes**
Abstract classes contain abstract methods, which are implemented by the derived class. The derived classes have more specialized functionality.

### ***rules about abstract classes***
1. You cannot create an instance of an abstract class
2. You cannot declare an abstract method outside an abstract class
3. When a class is declared sealed, it cannot be inherited, abstract classes cannot be declared sealed.


***To learn more*** [OOP](https://www.tutorialspoint.com/human_computer_interface/object_oriented_programming.htm)








