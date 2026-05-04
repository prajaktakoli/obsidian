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