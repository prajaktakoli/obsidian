## ✅ 1. **Encapsulation**

> Wrapping data (variables) and code (methods) into a single unit called a class.
> ✅ Encapsulation hides internal state and allows controlled access.
> Access modifiers are used

## ✅ 2. **Inheritance**

> When one class inherits from another (parent-child relationship).
> extends keyword is used is used

## ✅ 3. **Polymorphism**

> Same method, different behavior.
> 🔸 Compile-time (Overloading)
> 🔸 Runtime (Overriding) - override keyword is used

## ✅ 4. **Abstraction**

> Hiding implementation details and showing only functionality.
> Use Abstract classes and Interfaces

## 🔹 **5. Classes and Objects**

> A class is a blueprint; an object is an instance of a class.

## 🔹 **6. Constructors**

> Special methods used to initialize objects.
### 🔸 Types:

- **Default constructor** (no args)
- **Parameterized constructor**
- **Constructor overloading**
- **Constructor chaining** using `this()`
## 🧱 Java Constructors

### 🔹 What is a Constructor?
- Special method that is called **when an object is created**
- It **initializes** the object
- Constructor name = class name
- No return type (not even void)

---

### 🔹 Types of Constructors

#### ✅ 1. Default Constructor (No-args)
- Automatically provided by Java **if no constructor is defined**
- Initializes fields to default values (0, null, false)

```java
class Car {
    String model;
    Car() {
        System.out.println("Default constructor");
    }
}
```
#### ✅ 2. Parameterized Constructor
- Accepts arguments to initialize fields with custom values
#### ✅ 3. Constructor Overloading
- Multiple constructors in the same class
- Differ by **number/type/order of parameters**

#### ✅ 4. Constructor Chaining using `this()`
- One constructor calls another constructor in **same class**
- Must be **first line** in constructor
- `this()` must be the **first statement**
- You **cannot call multiple constructors** with multiple `this()` in one constructor
    

## 🔐 Access Modifiers

### 🟢 1. public
- Accessible **everywhere** (within and outside package)

### 🟡 2. protected
- Accessible in the **same package** and in **subclasses** (even outside the package)

### 🟠 3. default (package-private)
- Accessible only **within the same package**

### 🔴 4. private
- Accessible **only within the class**

### 🔸 Example:
```java
public class A {
    private int a = 1;
    int b = 2;           // default
    protected int c = 3;
    public int d = 4;

    public void show() {
        System.out.println(a + b + c + d);
    }
}
```

## 📍 this Keyword

### 🔹 What is `this`?
- Refers to the **current object**
- Resolves conflicts between class fields and method parameters
- Used to call another constructor from a constructor

### 🔸 Example:
```java
class Student {
    String name;
    Student(String name) {
        this.name = name;  // distinguishes field from parameter
    }
}
```
## 🧭 super Keyword

### 🔹 What is `super`?
- Refers to **parent class**
- Can be used to:
  - Access parent method/field
  - Call parent constructor (`super()`)

### 🔸 Example:
```java
class A {
    void greet() { System.out.println("Hello from A"); }
}

class B extends A {
    void greet() {
        super.greet(); // calls A’s greet()
        System.out.println("Hello from B");
    }
}
```
## 🔁 static Keyword

### 🔹 What is `static`?
- Belongs to **class**, not instance
- Shared across all instances
- Can be:
  - static variable
  - static method
  - static block

### 🔸 Example:
```java
class Counter {
    static int count = 0;
    Counter() {
        count++;
    }
}
```

## 🚫 final Keyword

### 🔹 What is `final` used for?
- Makes variables/constants unchangeable
- Prevents method overriding or class inheritance

### 🔸 Example:
```java
final class Vehicle { }  // can't be extended

final int MAX_SPEED = 120; // constant

class Bike {
    final void run() { }   // can't be overridden
}
```

### 🔹 What is a static block?
- A static block is a block of code enclosed in `static {}`.
- It runs **once when the class is loaded** (before `main()` or object creation).
- Used to initialize **static variables** or perform **one-time setup**.
```java
class Example {
    static int number;

    static {
        number = 42;
        System.out.println("Static block executed!");
    }

    public static void main(String[] args) {
        System.out.println("Main method: " + number);
    }
}
//Output:
//Static block executed!
//Main method: 42
```
