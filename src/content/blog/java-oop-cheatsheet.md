---
title: Java OOP Cheatsheet
author: Mahdin Ohi
pubDatetime: 2024-09-28T10:00:00
slug: java-oop
featured: false
draft: false
tags:
  - java
  - oop
  - cheatsheet
description: This Java cheatsheet offers a quick reference to essential syntax and commands, perfect for both beginners and experienced developers. Enhance your coding efficiency and master Java with this concise guide.
---

### Comprehensive Notes on Object-Oriented Programming (OOP) in Java

---

#### **1. Introduction to OOP**

Object-Oriented Programming (OOP) is a programming paradigm that relies on the concept of objects, which can contain data in the form of fields (attributes/properties) and code in the form of methods (functions). The four main principles of OOP are:

- **Encapsulation**
- **Abstraction**
- **Inheritance**
- **Polymorphism**

Java, being an OOP language, supports all of these concepts, and mastering them is essential for writing reusable, modular, and maintainable code.

---

### **2. Key OOP Principles in Java**

#### **2.1 Encapsulation**

Encapsulation refers to the bundling of data (attributes) and methods that operate on the data into a single unit called a class. It also involves restricting access to the internals of a class, exposing only what is necessary.

- **Private Fields**: Data is made private so it can only be accessed or modified through public methods.
- **Getters and Setters**: Public methods for accessing private fields.

**Example:**

```java
public class Person {
    private String name;
    private int age;

    // Getter
    public String getName() {
        return name;
    }

    // Setter
    public void setName(String name) {
        this.name = name;
    }

    // Getter
    public int getAge() {
        return age;
    }

    // Setter
    public void setAge(int age) {
        if (age > 0) {
            this.age = age;
        }
    }
}
```

#### **2.2 Abstraction**

Abstraction is the concept of hiding complex implementation details and showing only the essential features of an object. In Java, abstraction is achieved using abstract classes and interfaces.

- **Abstract Class**: A class that cannot be instantiated and may contain abstract methods.
- **Interface**: A completely abstract class, used to define a contract for classes.

**Example of Abstract Class:**

```java
abstract class Animal {
    abstract void sound();
    public void eat() {
        System.out.println("This animal is eating");
    }
}

class Dog extends Animal {
    public void sound() {
        System.out.println("Bark");
    }
}
```

**Example of Interface:**

```java
interface Drawable {
    void draw();  // Interface method
}

class Circle implements Drawable {
    public void draw() {
        System.out.println("Drawing Circle");
    }
}
```

#### **2.3 Inheritance**

Inheritance allows a new class (subclass) to inherit properties and behavior from an existing class (superclass), promoting code reuse.

- **Single Inheritance**: Java allows only single inheritance (one class can inherit from one superclass).
- **`extends` Keyword**: Used to inherit a class.
- **`super` Keyword**: Used to access superclass methods or constructors.

**Example:**

```java
class Animal {
    public void makeSound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Bark");
    }
}
```

#### **2.4 Polymorphism**

Polymorphism allows one interface to be used for a general class of actions. The specific action is determined by the exact nature of the situation.

- **Compile-Time Polymorphism (Method Overloading)**: Multiple methods in the same class with the same name but different parameters.
- **Run-Time Polymorphism (Method Overriding)**: Subclass provides a specific implementation of a method that is already defined by its superclass.

**Example of Method Overloading:**

```java
class MathOperation {
    public int add(int a, int b) {
        return a + b;
    }

    public int add(int a, int b, int c) {
        return a + b + c;
    }
}
```

**Example of Method Overriding:**

```java
class Animal {
    public void makeSound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Bark");
    }
}
```

---

### **3. Classes and Objects**

#### **3.1 Classes**

A class is a blueprint or prototype from which objects are created. It can contain fields (attributes) and methods to define behaviors.

**Example:**

```java
class Car {
    String model;
    String color;

    void drive() {
        System.out.println("The car is driving");
    }
}
```

#### **3.2 Objects**

An object is an instance of a class. When a class is instantiated, memory is allocated, and the instance is created.

**Example:**

```java
public class Main {
    public static void main(String[] args) {
        Car car = new Car(); // Creating an object
        car.model = "Tesla";
        car.color = "Red";
        car.drive();
    }
}
```

---

### **4. Constructors**

A constructor is a special method that is called when an object is instantiated. Its purpose is to initialize the object's state. Constructors do not have a return type.

- **Default Constructor**: Provided by Java if no constructor is defined.
- **Parameterized Constructor**: Accepts parameters to initialize object fields.

**Example of a Constructor:**

```java
class Car {
    String model;
    String color;

    // Constructor
    public Car(String model, String color) {
        this.model = model;
        this.color = color;
    }
}
```

---

### **5. Access Modifiers**

Access modifiers in Java determine the scope of variables, methods, and classes. They control the visibility of the code.

- **Private**: Accessible only within the same class.
- **Default (No Modifier)**: Accessible only within the same package.
- **Protected**: Accessible within the same package and by subclasses.
- **Public**: Accessible from any class.

**Example:**

```java
class Example {
    private int privateVar;
    public int publicVar;
    protected int protectedVar;
    int defaultVar;
}
```

---

### **6. Static Keyword**

- **Static Methods**: These methods belong to the class rather than instances of the class. They can be called without creating an object of the class.
- **Static Variables**: These variables are shared among all instances of a class.

**Example:**

```java
class Counter {
    static int count = 0;

    Counter() {
        count++;
        System.out.println(count);
    }
}
```

---

### **7. `this` and `super` Keywords**

- **`this`**: Refers to the current object.
- **`super`**: Refers to the superclass and is used to call superclass methods or constructors.

**Example of `this`:**

```java
class Person {
    String name;

    Person(String name) {
        this.name = name;  // Refers to the current object's name
    }
}
```

**Example of `super`:**

```java
class Animal {
    Animal() {
        System.out.println("Animal constructor");
    }
}

class Dog extends Animal {
    Dog() {
        super();  // Calls the superclass constructor
        System.out.println("Dog constructor");
    }
}
```

---

### **8. Final Keyword**

The `final` keyword can be applied to variables, methods, and classes.

- **Final Variable**: Its value cannot be changed (acts as a constant).
- **Final Method**: Cannot be overridden by subclasses.
- **Final Class**: Cannot be inherited by other classes.

**Example:**

```java
final class Constants {
    public static final double PI = 3.14159;
}
```

---

### **9. Abstract Classes vs Interfaces**

| Feature     | Abstract Class                              | Interface                                                          |
| ----------- | ------------------------------------------- | ------------------------------------------------------------------ |
| Methods     | Can have both abstract and concrete methods | Only abstract methods (Java 7); can have default methods (Java 8+) |
| Inheritance | A class can inherit only one abstract class | A class can implement multiple interfaces                          |
| Constructor | Can have a constructor                      | Cannot have a constructor                                          |
| Usage       | When you want to share common behavior      | When you want to define a contract                                 |

---

### **10. Conclusion**

Mastering OOP in Java is essential for building scalable, modular, and maintainable applications. The key concepts—encapsulation, abstraction, inheritance, and polymorphism—provide the foundation for writing reusable code that is easy to understand and extend.
