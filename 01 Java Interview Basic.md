### 1. **What is Java?**
   - **Answer:** Java is a high-level, object-oriented programming language developed by Sun Microsystems. It is designed to be platform-independent and follows the "Write Once, Run Anywhere" (WORA) principle.

### 2. **Explain the main features of Java.**
   - **Answer:** Key features of Java include:
     - Object-oriented
     - Platform-independent (via the Java Virtual Machine)
     - Simple and easy to learn
     - Distributed computing support (via RMI and EJB)
     - Multi-threading
     - Robust and secure (garbage collection, exception handling, etc.)
     - Dynamic and extensible

### 3. **What is the difference between `==` and `.equals()` in Java?**
   - **Answer:** 
     - `==` is used for comparing primitive data types or checking if two references point to the same object.
     - `.equals()` is a method used for comparing the content or values of objects. It's usually overridden in custom classes for meaningful comparison.

### 4. **What is the Java Virtual Machine (JVM)?**
   - **Answer:** JVM is a virtual machine that enables Java applications to run on any device or operating system. It provides an abstraction layer between the Java program and the underlying hardware and operating system.

### 5. **What is the difference between `abstract class` and `interface`?**
   - **Answer:**
     - An abstract class can have both abstract and concrete methods, while an interface can only have abstract methods.
     - A class can extend only one abstract class, but it can implement multiple interfaces.
     - Abstract classes can have constructors, while interfaces cannot.

### 6. **Explain the concept of multithreading in Java.**
   - **Answer:** Multithreading in Java is a feature that allows concurrent execution of two or more threads. Each thread runs independently, and Java provides built-in support for multithreading with the `Thread` class and `Runnable` interface.

### 7. **What is the Java Collections Framework?**
   - **Answer:** The Java Collections Framework provides a set of interfaces and classes for managing and manipulating groups of objects. It includes interfaces like List, Set, and Map, along with their implementing classes such as ArrayList, HashSet, and HashMap.

### 8. **What is the difference between `String`, `StringBuilder`, and `StringBuffer`?**
   - **Answer:**
     - `String` is immutable, meaning its value cannot be changed once it's assigned.
     - `StringBuilder` and `StringBuffer` are mutable and can be modified. `StringBuilder` is not thread-safe, while `StringBuffer` is thread-safe.

### 9. **What is the purpose of the `finalize()` method?**
   - **Answer:** The `finalize()` method is called by the garbage collector before an object is reclaimed. It allows the object to perform cleanup operations, such as releasing resources or closing connections.

### 10. **Explain the concept of exception handling in Java.**
   - **Answer:** Exception handling in Java is done through try, catch, and finally blocks. The `try` block contains the code that might throw an exception, the `catch` block catches and handles the exception, and the `finally` block contains code that is executed regardless of whether an exception is thrown or not.

