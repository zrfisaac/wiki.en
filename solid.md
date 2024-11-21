# SOLID

The **SOLID** principles are five fundamental principles in object-oriented programming that help create systems that are easier to maintain, flexible, and scalable. These principles promote good design practices and make it easier to develop and maintain high-quality code.

## Table of Contents

- [Single Responsibility Principle (SRP)](solid-srp)  
  The Single Responsibility Principle states that a class should have only one reason to change, meaning it should be responsible for only one part of the system's functionality.

- [Open/Closed Principle (OCP)](solid-ocp)  
  The Open/Closed Principle asserts that a class should be open for extension but closed for modification, allowing the behavior of a class to be extended without changing its original code.

- [Liskov Substitution Principle (LSP)](solid-lsp)  
  The Liskov Substitution Principle indicates that objects of a derived class should be able to replace objects of the base class without affecting the correctness of the program.

- [Interface Segregation Principle (ISP)](solid-isp)  
  The Interface Segregation Principle suggests that many client-specific interfaces are better than one general-purpose interface. Classes should not be forced to implement methods they do not use.

- [Dependency Inversion Principle (DIP)](solid-dip)  
  The Dependency Inversion Principle suggests that high-level modules should not depend on low-level modules. Both should depend on abstractions, and abstractions should not depend on details, but details should depend on abstractions.

---

## Single Responsibility Principle (SRP)

The **Single Responsibility Principle** (SRP) states that a class should have only one reason to change. This means that a class should be responsible for one and only one part of the functionality of the system, making the code easier to understand and maintain.

Example:

```csharp
// Class with a single responsibility: Managing Users
public class UserManager
{
    public void CreateUser(string name, string email)
    {
        // logic to create a user
    }
    
    public void DeleteUser(int userId)
    {
        // logic to delete a user
    }
}
```

---

## Open/Closed Principle (OCP)

The **Open/Closed Principle** (OCP) states that a class should be open for extension but closed for modification. This means that we should extend a class to change its behavior, without modifying its original code.

Example:

```csharp
public abstract class Shape
{
    public abstract double Area();
}

public class Circle : Shape
{
    public double Radius { get; set; }
    
    public override double Area()
    {
        return Math.PI * Radius * Radius;
    }
}

public class Square : Shape
{
    public double Side { get; set; }
    
    public override double Area()
    {
        return Side * Side;
    }
}
```

---

## Liskov Substitution Principle (LSP)

The **Liskov Substitution Principle** (LSP) states that objects of a derived class should be able to substitute objects of the base class without altering the correctness of the program. A derived class should inherit and reuse the behaviors of its base class without breaking functionality.

Example:

```csharp
public class Bird
{
    public virtual void Fly()
    {
        Console.WriteLine("Flying...");
    }
}

public class Sparrow : Bird
{
    public override void Fly()
    {
        Console.WriteLine("Sparrow flying...");
    }
}

public class Penguin : Bird
{
    // Here, we do not violate LSP because Penguin does not fly
    public override void Fly()
    {
        throw new NotImplementedException("Penguins cannot fly.");
    }
}
```

---

## Interface Segregation Principle (ISP)

The **Interface Segregation Principle** (ISP) suggests that many client-specific interfaces are better than one general-purpose interface. Classes should not be forced to implement methods they do not use, making the system more flexible and reducing unnecessary code.

Example:

```csharp
public interface IPrinter
{
    void Print();
}

public interface IScanner
{
    void Scan();
}

public class Printer : IPrinter
{
    public void Print() 
    {
        Console.WriteLine("Printing...");
    }
}

public class Scanner : IScanner
{
    public void Scan() 
    {
        Console.WriteLine("Scanning...");
    }
}
```

---

## Dependency Inversion Principle (DIP)

The **Dependency Inversion Principle** (DIP) suggests that high-level classes should not depend on low-level classes. Both should depend on abstractions. Abstractions should not depend on details, but details should depend on abstractions.

Example:

```csharp
public interface IWriter
{
    void Write(string message);
}

public class FileWriter : IWriter
{
    public void Write(string message)
    {
        // write to a file
        Console.WriteLine($"Writing to file: {message}");
    }
}

public class DatabaseWriter : IWriter
{
    public void Write(string message)
    {
        // write to a database
        Console.WriteLine($"Writing to database: {message}");
    }
}

public class MessageService
{
    private IWriter _writer;

    public MessageService(IWriter writer)
    {
        _writer = writer;
    }

    public void WriteMessage(string message)
    {
        _writer.Write(message);
    }
}
```

