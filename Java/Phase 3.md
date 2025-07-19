# 🧠 Java Lesson 4 – Memory Management & Exception Handling

---

## 🧮 Java Memory Areas (JVM Architecture)

### 🔸 1. Heap Memory
- Stores **objects** and **instance variables**
- Shared across all threads
- Managed by Garbage Collector (GC)

### 🔸 2. Stack Memory
- Stores **method calls**, **local variables**
- Each thread has its own stack
- Follows **LIFO** (Last-In-First-Out)

### 🔸 3. Method Area (MetaSpace in Java 8+)
- Stores class definitions, static variables, constants

### 🔸 4. PC Register
- Stores address of current thread’s instruction

### 🔸 5. Native Method Stack
- Used for native (non-Java) code via JNI

---

## 🚮 Java Garbage Collection

### 🔹 GC Reclaims memory of unreachable objects in the heap

### 🔸 `System.gc()` is just a suggestion, **not guaranteed**

### 🔸 Finalization:
```java
@Override
protected void finalize() throws Throwable {
    System.out.println("Object destroyed");
}
```
## 🚨 Exception Handling in Java

### 🔹 Exception = **Unexpected event** disrupting normal flow

### 🔸 Types:

- **Checked Exceptions** – must be handled at compile time (`IOException`, `SQLException`)
- **Unchecked Exceptions** – runtime errors (`NullPointerException`, `ArithmeticException`)

| throw    | To **explicitly throw** an exception            |
| -------- | ----------------------------------------------- |
| `throws` | Declares **which exception** method might throw |
📜 Custom Exceptions extends Exception 

## 🔢 17. Wrapper Classes & Autoboxing

### 🔹 What are Wrapper Classes?
- Classes that wrap primitive types into objects

| Primitive | Wrapper Class |
|-----------|----------------|
| `int`     | `Integer`      |
| `char`    | `Character`    |
| `double`  | `Double`       |
| `boolean` | `Boolean`      |

### 🔸 Why?
- Needed for **Collections**, **Object manipulation**

### 🔸 Autoboxing:
- Converting primitive → object automatically

```java
int a = 10;
Integer obj = a; // autoboxing
🔸 Unboxing:
Object → primitive automatically

Integer obj = 20;
int b = obj; // unboxing
```
## 🧊 18. Immutable Classes

### 🔹 Immutable = **State cannot be changed once created**

### 🔸 Example: `String` is immutable

### 🔸 How to Create Custom Immutable Class:
final class Employee {
    private final String name;
    public Employee(String name) {
        this.name = name;
    }
    public String getName() {
        return name;
    }
}
- Class must be `final`
- All fields must be `private final`
- No setters
- Provide only getters

| Feature     | String      | StringBuffer   | StringBuilder   |
| ----------- | ----------- | -------------- | --------------- |
| Mutability  | ❌ Immutable | ✅ Mutable      | ✅ Mutable       |
| Thread-safe | ✅ Yes       | ✅ Yes          | ❌ No            |
| Performance | 🚫 Slow     | 🟡 Medium      | ✅ Fast          |
| Best For    | Constants   | Multi-threaded | Single-threaded |