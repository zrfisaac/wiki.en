# Java

Welcome to the **Java Wiki**! This resource is designed to help developers understand and use Java for building robust, object-oriented applications.

## Description

Java is a high-level, object-oriented programming language developed by Sun Microsystems (now owned by Oracle). It is widely used for building cross-platform applications, web applications, mobile applications (via Android), and large-scale enterprise systems.

Java is known for its portability, scalability, and security. Its "Write Once, Run Anywhere" philosophy means that Java applications are compiled into bytecode that can run on any system that has a Java Virtual Machine (JVM), regardless of underlying hardware or operating system.

## Useful Links

- [Official Java Documentation](https://docs.oracle.com/en/java/)
- [Java GitHub Repository](https://github.com/openjdk/jdk)
- [Java Platform Overview](https://www.oracle.com/java/)
- [Java Tutorials](https://docs.oracle.com/javase/tutorial/)
- [Maven - Dependency Management for Java](https://maven.apache.org/)

## Table of Contents

- [Description](#description)
- [Useful Links](#useful-links)
- [Java Versions](#java-versions)
- [Basic Java Code Examples](#basic-java-code-examples)

## Java Versions

Java has undergone numerous updates since its initial release. Key versions include:

- **Java 1.0**  
  The first version of Java, released in 1996, established Java as a revolutionary new language designed for the internet.

- **Java 5 (J2SE 5.0)**  
  Released in 2004, this version introduced major features like generics, metadata annotations, enumerated types, and the enhanced for-loop.

- **Java 8**  
  Released in 2014, this version brought significant changes, including lambdas, streams, and the introduction of the `java.time` API for handling date and time.

- **Java 11**  
  Released in 2018, Java 11 is a long-term support (LTS) version that introduced several new features, including the `var` keyword for local variables, and enhanced security features.

- **Java 17**  
  Released in 2021, Java 17 is another LTS version and brings a variety of performance, security, and new language feature improvements.

For a complete list of Java versions, refer to the [Java Release Notes](https://www.oracle.com/java/technologies/javase-downloads.html).

## Basic Java Code Examples

Here are some basic Java code examples to help you get started:

**Hello World Program**  
The most basic Java program to print "Hello, World!" to the console.

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

**Class and Object Example**  
A simple example to demonstrate the creation of classes and objects in Java.

```java
class Car {
    String model;
    int year;

    // Constructor
    public Car(String model, int year) {
        this.model = model;
        this.year = year;
    }

    // Method
    public void displayInfo() {
        System.out.println("Model: " + model + ", Year: " + year);
    }
}

public class Main {
    public static void main(String[] args) {
        Car car = new Car("Toyota", 2020);
        car.displayInfo();
    }
}
```

**For-Each Loop Example**  
Demonstrates the use of the enhanced for-loop in Java.

```java
public class Main {
    public static void main(String[] args) {
        String[] fruits = {"Apple", "Banana", "Cherry"};
        for (String fruit : fruits) {
            System.out.println(fruit);
        }
    }
}
```

**Lambda Expression Example**  
A simple example of using a lambda expression for a functional interface.

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        List<String> names = Arrays.asList("Alice", "Bob", "Charlie");

        // Using a lambda expression to print names
        names.forEach(name -> System.out.println(name));
    }
}
```

**Try-Catch Exception Handling Example**  
Demonstrates how to handle exceptions in Java.

```java
public class Main {
    public static void main(String[] args) {
        try {
            int result = 10 / 0;
        } catch (ArithmeticException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```

**Creating and Running a Java Program**  
1. Write your Java code in a `.java` file (e.g., `HelloWorld.java`).
2. Compile the code using the following command:
   ```bash
   javac HelloWorld.java
   ```
3. Run the compiled code with the command:
   ```bash
   java HelloWorld
   ```

