| Term                               | Description                                               |
| ---------------------------------- | --------------------------------------------------------- |
| **JVM (Java Virtual Machine)**     | Runs your compiled `.class` bytecode. Platform-specific.  |
| **JRE (Java Runtime Environment)** | JVM + libraries (runtime only, no compiler).              |
| **JDK (Java Development Kit)**     | JRE + compiler + debugger + tools (used for development). |
🔸 **You write `.java` ➝ JDK compiles it to `.class` ➝ JVM runs the bytecode**

### 🔸 Primitive Types (stored directly):

🔸 Reference Types (store memory reference):
## ***Pass by Value***

All arguments in Java are passed **by value**, not by reference:

java

CopyEdit

`public static void change(int x) {     x = 100; }  public static void main(String[] args) {     int a = 10;     change(a);     System.out.println(a);  // Still prints 10 }`

> Even for objects, the reference is copied **by value**.

-----------------
## 🔹 **4. Type Casting**

### 🔸 Widening (implicit):

`int a = 10; long b = a;  // OK`

### 🔸 Narrowing (explicit):

`double d = 5.6; int i = (int) d; // 5`