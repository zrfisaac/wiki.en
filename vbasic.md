# Visual Basic

Welcome to the **Visual Basic Wiki**! This is your comprehensive resource for learning and mastering Visual Basic, one of the most widely used programming languages for developing Windows applications and automation solutions.

## Description

Visual Basic (VB) is a high-level programming language developed by Microsoft, known for its simplicity and ease of use. Initially created for graphical user interface (GUI) development, it has evolved to support object-oriented programming and other modern features. Visual Basic is widely used in enterprise systems, task automation, and Windows application development.

This wiki provides an introduction to Visual Basic, with code examples, best practices, and useful links to help you get started or improve your projects.

## Useful Links

- [Official Visual Basic Documentation](https://learn.microsoft.com/en-us/dotnet/visual-basic/)
- [Visual Basic on GitHub](https://github.com/dotnet/visualbasic)
- [Visual Basic Syntax Reference](https://learn.microsoft.com/en-us/dotnet/visual-basic/language-reference/)
- [Visual Basic Style Guide](https://learn.microsoft.com/en-us/dotnet/visual-basic/programming-guide/)
- [Visual Basic Code Samples](https://docs.microsoft.com/en-us/samples/browse/?languages=visual-basic)

## Table of Contents

- [Description](#description)
- [Useful Links](#useful-links)
- [Visual Basic Versions](#visual-basic-versions)
- [Basic Code Examples](#basic-code-examples)

## Visual Basic Versions

Visual Basic has gone through several versions since its release. Here are some of the most important milestones:

- **Visual Basic 6.0**  
  Released in 1998, it was widely used for Windows application development but was discontinued with the introduction of the .NET Framework.

- **Visual Basic .NET (VB.NET)**  
  Released in 2002 with the .NET Framework, it was a complete rewrite of the language to support object-oriented programming and the new Microsoft architecture.

- **VB 2010 - 2019**  
  Microsoft continued to evolve the language with improvements in LINQ support, async/await, and new features to facilitate desktop and web application development.

- **VB 2022**  
  The latest version, with ongoing performance improvements, compatibility with .NET 5 and beyond, and support for new development tools like MAUI.

For a detailed history of Visual Basic versions, visit the [Visual Basic Version Documentation](https://learn.microsoft.com/en-us/dotnet/visual-basic/language-reference/).

## Basic Code Examples

Here are a few examples to get started with Visual Basic:

**Hello, World Example**  
```vb
Module Module1
    Sub Main()
        Console.WriteLine("Hello, World!")
    End Sub
End Module
```

**Reading a Text File**  
```vb
Module Module1
    Sub Main()
        Dim content As String = System.IO.File.ReadAllText("example.txt")
        Console.WriteLine(content)
    End Sub
End Module
```

**Using a For Loop**  
```vb
Module Module1
    Sub Main()
        For i As Integer = 0 To 4
            Console.WriteLine("Iteration " & i)
        Next
    End Sub
End Module
```

**Simple Function**  
```vb
Module Module1
    Function Greeting(name As String) As String
        Return "Hello, " & name
    End Function

    Sub Main()
        Console.WriteLine(Greeting("Alice"))
    End Sub
End Module
```

**Creating a Class and Object**  
```vb
Module Module1
    Class Person
        Public Name As String

        Sub New(name As String)
            Me.Name = name
        End Sub

        Sub Greet()
            Console.WriteLine("Hello, " & Me.Name)
        End Sub
    End Class

    Sub Main()
        Dim person As New Person("Alice")
        person.Greet()
    End Sub
End Module
```

**Event Handling Example**  
```vb
Module Module1
    Event Greet As Action

    Sub Main()
        AddHandler Greet, AddressOf DisplayGreeting
        RaiseEvent Greet
    End Sub

    Sub DisplayGreeting()
        Console.WriteLine("Greeting received!")
    End Sub
End Module
```

