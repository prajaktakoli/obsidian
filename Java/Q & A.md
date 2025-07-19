# 🎯 Interview Questions (with answers)

### ✅ Encapsulation
- **Q:** Why do we use encapsulation?
- **A:** To protect data, reduce complexity, and enforce access control.

- **Q:** How is encapsulation implemented in Java?
- **A:** Using `private` fields with `public` getters and setters.

---

### ✅ Inheritance
- **Q:** Can Java support multiple inheritance?
- **A:** Not with classes. Java supports multiple inheritance with interfaces only.

- **Q:** What is the benefit of inheritance?
- **A:** Code reuse and polymorphism.

---

### ✅ Polymorphism
- **Q:** What is the difference between overloading and overriding?
- **A:** Overloading happens in the same class with different parameters; overriding in subclasses with same method signature.

- **Q:** What is dynamic method dispatch?
- **A:** Runtime decision of which overridden method to call based on object type.

---

### ✅ Abstraction
- **Q:** What is the difference between abstract class and interface?
- **A:** Abstract class can have both abstract and non-abstract methods; interface can only have abstract methods (till Java 7), Java 8+ allows default/static.

- **Q:** When do you use abstraction?
- **A:** When you want to define a contract without implementation.
- 
### 🔐 Access Modifiers
- **Q:** What is the difference between private and default?
  - **A:** `private` = only inside the class. `default` = accessible inside the package.

- **Q:** Which modifier gives the most restricted access?
  - **A:** `private`.

---

### 📍 this
- **Q:** Why is `this` keyword used?
  - **A:** To refer to the current class object and resolve naming conflicts.

---

### 🧭 super
- **Q:** Can you call a superclass constructor using `super()`?
  - **A:** Yes, but it must be the **first statement** in the subclass constructor.

---

### 🔁 static
- **Q:** Can static methods access non-static variables?
  - **A:** No, because static methods don’t belong to any instance.

---

### 🚫 final
- **Q:** Can you override a final method?
  - **A:** No. Final methods can't be overridden.
  
### ✅ Q1: When is a static block executed?
**A:** When the class is **loaded into JVM**, before any object is created and before the main method.

---

### ✅ Q2: Can you have multiple static blocks?
**A:** Yes. They execute **in the order they appear** in the source code.

---

### ✅ Q3: What is the difference between static block and static method?
| Feature        | Static Block                 | Static Method              |
|----------------|------------------------------|----------------------------|
| When it runs   | When class loads             | When explicitly called     |
| Return type    | No                           | Yes (has return type)      |
| Use case       | Initialization               | Utility logic              |
### ✅ Java Memory Management

**Q1:** What is the difference between stack and heap memory?  
**A:** Stack holds method calls and local variables; heap stores objects and instance variables.

**Q2:** When is an object eligible for garbage collection?  
**A:** When no reference points to it.

**Q3:** What is the role of `finalize()` method?  
**A:** It's called before the object is garbage collected (deprecated in Java 9).

---

### ✅ Exception Handling

**Q1:** What is the difference between checked and unchecked exceptions?  
**A:** Checked = handled at compile time; Unchecked = runtime errors.

**Q2:** Can you have multiple catch blocks?  
**A:** ✅ Yes, from most specific to most generic.

**Q3:** What happens if an exception is not caught?  
**A:** The program terminates abruptly and prints a stack trace.

**Q4:** Can `finally` block be skipped?  
**A:** Only if JVM exits using `System.exit()` or crashes.

**Q5:** Can you catch multiple exceptions in one catch?  
**A:** ✅ Yes, using multi-catch syntax `catch (IOException | SQLException e)`.

**Q6:** Can you throw exceptions manually?  
**A:** ✅ Yes, using `throw new Exception("error")`.

**Q1:** Why are wrapper classes used?  
**A:** To use primitives with collections and treat them as objects.

**Q2:** What is autoboxing/unboxing?  
**A:** Automatic conversion between primitives and wrapper types.

**Q1:** Why should a class be immutable?  
**A:** For thread-safety, caching, and security.

**Q2:** Can you change a string once created?  
**A:** ❌ No. `String` is immutable.

**Q1:** Difference between StringBuilder and StringBuffer?  
**A:** Both are mutable. `StringBuffer` is thread-safe; `StringBuilder` is faster but not thread-safe.

**Q2:** Which is better for multi-threaded programs?  
**A:** `StringBuffer`.

**Q1:** What's the difference between List and Set?  
**A:** List allows duplicates and maintains insertion order. Set doesn't allow duplicates.

**Q2:** When would you use a Map over a List?  
**A:** Use Map for key-value pairs (like a dictionary), List for ordered values.

**Q3:** Is Queue part of List?  
**A:** ❌ No. Queue and List both extend Collection but serve different purposes.

**Q4:** ArrayList vs LinkedList?  
**A:**

- ArrayList: Fast `get(index)`, slow `add(index)`
- LinkedList: Slow `get(index)`, fast `add/remove`
- 
**Q5:** HashSet vs TreeSet?  
**A:**

- HashSet: Unordered, faster
- TreeSet: Sorted, slower

