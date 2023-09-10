# Using OOP concepts to write high-performance Java code (2023)

## List of OOP concepts in Java:
- Abstraction
- Encapsulation
- Inheritance
- Polymorphism
- Association
- Aggregation
- Composition

# What are OOP concepts in Java?
 - Object-oriented programming focuses on objects made up of both data (fields) and code (properties or attributes). 
 - Java supports object-oriented programming
    
# Advantages of OOP
- Classes provide easy “building blocks” for faster coding and make code highly maintainable
- Create more stable and consistent code
- Make large and complex code bases more efficient and manageable
- Teams working from the same code base will benefit from existing well-written classes
- Java in particular enforces OOP, which creates good habits (but may be challenging for beginners)

# Definitions of OOP concepts

## 1. Abstraction
- Abstraction aims to hide complexity from users and show them only relevant information. For example, if you’re driving a car, you don’t need to know about its internal workings.

### Abstraction in Java
- Hides the underlying complexity of data
- Helps avoid repetitive code
- Presents only the signature of internal functionality
- Gives flexibility to programmers to change the implementation of abstract behavior
- Partial abstraction (0-100%) can be achieved with abstract classes
- Total abstraction (100%) can be achieved with interfaces
  
### Abstract classes
An abstract class is a superclass (parent class) that cannot be instantiated. To create a new object, you need to instantiate one of its child classes. Abstract classes can have both abstract and concrete methods. Abstract methods contain only the method signature, while concrete methods declare the method body as well. Abstract classes are defined with the abstract keyword.

### Interfaces
An interface is a 100% abstract class. It can only have static, final, and public fields and abstract methods. It’s frequently referred to as a blueprint of a class as well. Java interfaces allow you to implement multiple inheritances in your code, as a class can implement any number of interfaces. Classes can access an interface with the implements keyword.

## 2. Encapsulation
- Encapsulation helps with data security, allowing you to protect the data stored in a class from system-wide access. As the name suggests, it safeguards the internal contents of a class like a capsule.
- You can implement encapsulation in Java by making the fields (class variables) private and accessing them via their public getter and setter methods. JavaBeans are examples of fully encapsulated classes.

### Encapsulation in Java:

- Restricts direct access to data members (fields) of a class
- Fields are set to private
- Each field has a getter and setter method
- Getter methods return the field
- Setter methods let us change the value of the field


## 3. Inheritance
- Inheritance makes it possible to create a child class that inherits the fields and methods of the parent class. The child class can override the values and methods of the parent class, but it’s not necessary. It can also add new data and functionality to its parent.
- Parent classes are also called superclasses or base classes, while child classes are known as subclasses or derived classes as well. Java uses the extends keyword to implement the principle of inheritance in code.



### Inheritance in Java:

- A class (child class) can extend another class (parent class) by inheriting its features
- Implements the DRY (Don’t Repeat Yourself) programming principle
- Improves code reusability
- Multi-level inheritance is allowed in Java (a child class can have its own child class as well)
- Multiple inheritances are not allowed in Java (a class can’t extend more than one class)

### 4. Polymorphism
- Polymorphism refers to the ability to perform a certain action in different ways. In Java, polymorphism can take two forms: method overloading and method overriding.
- Method overloading happens when various methods with the same name are present in a class. When they are called, they are differentiated by the number, order, or types of their parameters. Method overriding occurs when a child class overrides a method of its parent.

### Polymorphism in Java:

- The same method name is used several times
- Different methods of the same name can be called from an object
- All Java objects can be considered polymorphic (at the minimum, they are of their own type and instances of the Object class)
- Static polymorphism in Java is implemented by method overloading
- Dynamic polymorphism in Java is implemented by method overriding


Function overloading and function overriding are both concepts used in object-oriented programming languages like Java and C++. They involve creating multiple functions with the same name but with different behaviors. Here's an example illustrating the difference between function overloading and function overriding in Java:

Function Overloading:
Function overloading occurs within a single class, and it involves defining multiple methods with the same name in that class. These methods must have different parameter lists (different types or different numbers of parameters). The appropriate method is chosen at compile time based on the arguments provided when calling the function.

```java
ass Calculator {
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }
}

public class Main {
    public static void main(String[] args) {
        Calculator calc = new Calculator();
        
        int result1 = calc.add(3, 4);          // Calls the first add method
        double result2 = calc.add(2.5, 3.7);   // Calls the second add method

        System.out.println("Result 1: " + result1);
        System.out.println("Result 2: " + result2);
    }
}
```

In this example, the Calculator class has two add methods with different parameter types (int and double). The appropriate method is called based on the argument types when invoking the add function.

Function Overriding:
Function overriding, on the other hand, is a concept related to inheritance. It occurs when a subclass provides a specific implementation for a method that is already defined in its superclass. The method in the subclass must have the same name, return type, and parameters (or a subtype) as the method in the superclass. This allows a subclass to provide its own behavior while still adhering to the method signature of the superclass.


```java


class Shape {
    void draw() {
        System.out.println("Drawing a shape");
    }
}

class Circle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing a circle");
    }
}

public class Main {
    public static void main(String[] args) {
        Shape shape = new Circle();
        shape.draw(); // Calls the overridden method in Circle
    }
}
In this example, the Circle class extends the Shape class and overrides the draw method. When we create a Circle object and call the draw method, it executes the overridden method in the Circle class, not the one in the Shape class.

```java
class Calculator {
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }
}
```
  
  
### Notes: 
- This Article is Quoted from RAYGUN, But i try to summarize it as much as posssible for fellow GitHub Friends.
- You Can Find the Original Article On: [RAYGUN](https://raygun.com/blog/oop-concepts-java/#composition)
