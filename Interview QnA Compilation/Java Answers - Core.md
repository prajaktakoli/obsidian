OOPs
# . Encapsulation (Data Hiding)

👉 **Idea:** Wrap data + methods together and restrict direct access.
### 🧠 Real-world Example:

Think of a **Bank Account**
- You **can’t directly access balance**
- You use methods like `deposit()` / `withdraw()`

---

### 💻 Java Example:

```
class BankAccount {    private double balance;  // hidden data    public void deposit(double amount) {        balance += amount;    }    public double getBalance() {        return balance;    }}
```

### ✅ Key Points:

- Use `private` variables
- Provide `getter/setter`
- Improves security & control
# 2. Abstraction (Hiding Implementation)

👉 **Idea:** Show only essential details, hide internal logic.
### 🧠 Real-world Example:
Driving a **Car**
- You use steering, brake, accelerator
- You don’t know engine internals
- 
abstract class Vehicle {
    abstract void start();  // only definition
}

class Car extends Vehicle {
    void start() {
        System.out.println("Car starts with key");
    }
}
# 3. Inheritance (Code Reusability)

👉 **Idea:** One class inherits properties of another.
### 🧠 Real-world Example:
**Animal → Dog**
- Dog inherits eating, breathing from Animal
# 4. Polymorphism (Many Forms)

👉 **Idea:** Same method behaves differently.
## A) Compile-time (Method Overloading)

```
class MathUtils {    int add(int a, int b) {        return a + b;    }    double add(double a, double b) {        return a + b;    }}
```
## B) Runtime (Method Overriding)

### 🧠 Real-world Example:

**Payment System**

- CreditCard → different logic
- UPI → different logic
- 
Think of **Amazon App**:

- Encapsulation → User data hidden
- Abstraction → UI hides backend logic
- Inheritance → Seller/User classes extend base class
- Polymorphism → Different payment methods behave differently
---------------
Access Modifiers:
Private : Same class
Public : Accessible everywhere
Protected : Same class, Same package and SUbclass in other package 
Default : Same class and Same package
_________
This : current class object
Super : Parent class object
____
Checked Exception : Checked at Compile Time, need to use try-catch/throws - IOException, SQLException
Unchecked Exception : Occurs at Runtime - NullPointerException

-------
Stream API :
 Process collections in a **functional style (no loops)** → `filter()`, `map()`, `reduce()`, `collect()`

```
List<Integer> nums = List.of(1,2,3,4);
nums.stream()    
.filter(n -> n % 2 == 0)   // 2,4    
.map(n -> n * 2)           // 4,8    
.forEach(System.out::println);
```

Lambda Expression
**Short way to write anonymous functions**

```
(a, b) -> a + b
```
Functional Interfaces
- Interface with **only one abstract method**
- `Predicate<T>` → returns boolean
- `Function<T, R>` → input → output
- `Consumer<T>` → takes input, no return
- `Supplier<T>` → no input, returns value

Optional API

- Avoids **NullPointerException**

```
Optional<String> name = Optional.ofNullable(null);
System.out.println(name.orElse("Default"));
```

Heap Vs Stack
- **Stack** → Stores _method calls & local variables_ (fast, auto-managed, thread-specific)
- **Heap** → Stores _objects & instance data_ (shared, larger, managed by GC)

String vs StringBuilder vs String Buffer
- **String** → Immutable, thread-safe (because immutable), slower for frequent changes
- **StringBuilder** → Mutable, _not thread-safe_, fastest for modifications
- **StringBuffer** → Mutable, _thread-safe (synchronized)_, slower than StringBuilder
- https://javaconceptoftheday.com/java-strings-cheat-sheet/
----------------
#### COLLECTIONS
https://javaconceptoftheday.com/java-collections-cheat-sheet/

#### QUESTIONS
### Comparable vs Comparator : 

Comparable : Natural Ordering : 
Used when a class defines its **default/natural sorting logic**
CompareTo()

Comparator : Custom Ordering
Used when you want **multiple/dynamic sorting logics**
Compare()

