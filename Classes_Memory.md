# Classes & Memory Management

## class 
It's a blueprint for a data type.
A class definition starts with the keyword class followed by the class name; and the class body enclosed by a pair of curly braces.

Note −

Access specifiers specify the access rules for the members as well as the class itself. If not mentioned, then the default access specifier for a class type is internal. Default access for the members is private.

Data type specifies the type of variable, and return type specifies the data type of the data the method returns, if any.

To access the class members, you use the dot (.) operator.

The dot operator links the name of an object with the name of a member.

## Constructor

A class constructor is a special member function of a class that is executed whenever we create new objects of that class.

A constructor has exactly the same name as that of class and it does not have any return type.

A **default constructor** does not have any parameter but if you need, a constructor can have parameters. Such constructors are called **parameterized constructors**. This technique helps you to assign initial value to an object at the time of its creation.

## Object 

An object is an instance of a class

In C#, here's how we create an object of the class.
ClassName obj = new ClassName();

We use the name of objects along with the (.) operator to access members of a class.

***To learn More*** [Object and Class](https://www.javatpoint.com/c-sharp-object-and-class)