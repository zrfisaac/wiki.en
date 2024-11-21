# C#

Welcome to the **C# Wiki**! This is a comprehensive resource for developers working with C#, offering insights, tips, and examples to help you maximize your development capabilities.  

## Description  

C# is a modern, object-oriented programming language developed by Microsoft as part of the .NET platform. It is versatile, efficient, and widely used for building desktop, web, and mobile applications. With its extensive libraries and support for cross-platform development via .NET Core and .NET 6/7, C# empowers developers to create robust, scalable, and maintainable solutions.  

This wiki serves as a central hub to explore C# features, understand its capabilities, and access valuable resources to enhance your projects.  

## Useful Links  

- [Official C# Documentation](https://learn.microsoft.com/en-us/dotnet/csharp/)  
- [Microsoft Learn - .NET](https://learn.microsoft.com/en-us/dotnet/)  
- [GitHub - .NET Repository](https://github.com/dotnet/)  
- [NuGet Package Manager](https://www.nuget.org/)  
- [C# Coding Standards](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions)  

## Index  

- [Description](#description)  
- [Useful Links](#useful-links)  
- [C# Versions](#csharp-versions)  
- [Examples of Basic Code](#examples-of-basic-code)  

## C# Versions  

C# has evolved significantly since its first release. Here are some key milestones:  

- **C# 1.0**  
  Introduced in 2002 with .NET Framework 1.0, providing basic object-oriented programming capabilities.  

- **C# 3.0**  
  Added LINQ (Language Integrated Query), lambda expressions, and extension methods.  

- **C# 5.0**  
  Introduced async/await for asynchronous programming, streamlining modern application development.  

- **C# 8.0**  
  Introduced nullable reference types, ranges, and switch expressions, improving code safety and readability.  

- **C# 10.0**  
  Featured global usings, file-scoped namespaces, and record structs, simplifying code structure.  

- **C# 11.0**  
  Latest version with enhanced pattern matching, list patterns, and static abstract members in interfaces.  

For a detailed list of versions and their release notes, visit the [C# Language Version History](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/).  

## Examples of Basic Code  

Here are some basic C# code snippets to help you get started:  

**Hello World Example**  
```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, World!");
    }
}
```

**Simple Form with a Button (WinForms)**  
```csharp
using System;
using System.Windows.Forms;

public class MainForm : Form
{
    private Button button;

    public MainForm()
    {
        button = new Button();
        button.Text = "Click Me";
        button.Click += (sender, e) => MessageBox.Show("Button clicked!");
        Controls.Add(button);
    }

    [STAThread]
    public static void Main()
    {
        Application.Run(new MainForm());
    }
}
```

**Connecting to a Database with ADO.NET**  
```csharp
using System;
using System.Data.SqlClient;

class Program
{
    static void Main()
    {
        string connectionString = "Server=your_server;Database=your_database;User Id=your_username;Password=your_password;";

        using (SqlConnection connection = new SqlConnection(connectionString))
        {
            connection.Open();
            Console.WriteLine("Database connected successfully!");

            string query = "SELECT * FROM your_table";
            using (SqlCommand command = new SqlCommand(query, connection))
            using (SqlDataReader reader = command.ExecuteReader())
            {
                while (reader.Read())
                {
                    Console.WriteLine(reader[0]); // Print the first column of each row
                }
            }
        }
    }
}
```
