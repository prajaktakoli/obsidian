JVM is platform dependent
Java is not
JVM understands only bytecode, so java code needs to be convert into byte code which is a compiler so javac is used and then bytecode will run on jvm
main function is needed

in java, everything should be an object. It also means that evrything should be in a class
- Extension for bytecode - .class and java code is - .java
Commands 
javac hello.java ( hello is filename) : it is used for compilation
java Hello (Hello is classname) :  used to run code
![[Pasted image 20241218160528.png]]


### JVM (Java Virtual Machine)

- **Definition**: Runs Java bytecode and provides an environment for Java applications.
- **Role**: Executes compiled `.class` files (bytecode).
- **Components**: Includes a Just-In-Time (JIT) compiler for optimization.
- **Example**: Converts `System.out.println("Hello");` from bytecode to machine code.

### JRE (Java Runtime Environment)

- **Definition**: Provides the libraries and JVM necessary to run Java applications.
- **Role**: Enables running precompiled Java programs but doesn't include development tools.
- **Components**: Includes JVM + standard Java libraries.
- **Use Case**: Use it when you want to execute Java programs without writing code.

### JDK (Java Development Kit)

- **Definition**: A complete development toolkit for Java.
- **Role**: Allows developing, compiling, and running Java applications.
- **Components**: Includes JRE + development tools (compiler `javac`, debugger, etc.).
- **Use Case**: Required for developers writing and compiling Java programs.

### Analogy

- **JVM**: Like a chef (executor).
- **JRE**: Like a fully equipped kitchen (execution-only).
- **JDK**: Like a kitchen + grocery store (development + execution).
-------------
data types - int, byte, short, long, float, decimal, char, boolean
for binary :
int num = 0b101; --> 5
int num = 0x7E --> 126
int num = 100_00_000
double num = 12e10 --> 1.2e11

-----------
Type conversion and casting
Implicit (from byte to int) and explicit (int to byte) 
eg. (byte)a

byte b = 126;
int a = 257
b = (byte) a
in this case : it will convert 257 %256(256 means the range of byte -128 to 127) and b will be = 1;
