# ASP.NET

ASP.NET is an open-source framework for building dynamic web applications. Created by Microsoft, it facilitates the creation of scalable, high-performance web applications. ASP.NET supports several programming languages, but C# is the most commonly used.

---

## Table of Contents

- [Prerequisites](#prerequisites)  
  Configuration to start using ASP.NET in your development environment.

- [Basic ASP.NET Concepts](#basic-asp-net-concepts)  
  Overview of fundamental ASP.NET concepts like controllers, views, and models.

- [ASP.NET Example](#asp-net-example)  
  A simple example to create a basic application, including setting up a controller and a view.

- [Advanced ASP.NET Concepts](#advanced-asp-net-concepts)  
  More advanced topics like authentication, middleware, and RESTful APIs.

---

## Prerequisites

To start using ASP.NET, you'll need a few prerequisites installed on your computer:

1. **.NET SDK**:  
   Download and install the .NET SDK from the [official website](https://dotnet.microsoft.com/download).

2. **Code Editor**:  
   You can use Visual Studio, Visual Studio Code, or another editor that supports .NET. Visual Studio is highly recommended for most users as it provides advanced debugging and UI design features.

   - **Install Visual Studio**:  
     Download Visual Studio from [visualstudio.microsoft.com](https://visualstudio.microsoft.com/). During installation, select the "ASP.NET and web development" option.

3. **Database (Optional for Database Examples)**:  
   To use ASP.NET with a database, you can use SQL Server, PostgreSQL, MySQL, among others. Entity Framework is the main ORM (Object-Relational Mapping) tool for ASP.NET.

---

## Basic ASP.NET Concepts

### Controllers

Controllers in ASP.NET are responsible for handling HTTP requests, processing business logic, and returning a response to the user. They are the core part of the MVC (Model-View-Controller) pattern.

```csharp
using Microsoft.AspNetCore.Mvc;

namespace MyApp.Controllers
{
    public class HomeController : Controller
    {
        public IActionResult Index()
        {
            return View();
        }

        public IActionResult Greet(string name)
        {
            ViewData["Message"] = $"Hello, {name}!";
            return View();
        }
    }
}
```

### Views

Views in ASP.NET are files that contain the user interface for the application. They are responsible for displaying the data that the controller sends.

```html
<!-- Views/Home/Index.cshtml -->
<!DOCTYPE html>
<html>
<head>
    <title>Welcome to ASP.NET</title>
</head>
<body>
    <h1>Welcome to the ASP.NET application!</h1>
</body>
</html>

<!-- Views/Home/Greet.cshtml -->
<!DOCTYPE html>
<html>
<head>
    <title>Greeting</title>
</head>
<body>
    <h1>@ViewData["Message"]</h1>
</body>
</html>
```

### Models

Models in ASP.NET represent the application's data and business logic. In many applications, models are used to interact with the database.

```csharp
namespace MyApp.Models
{
    public class Person
    {
        public string Name { get; set; }
        public int Age { get; set; }
    }
}
```

---

## ASP.NET Example

Here's a simple example of an ASP.NET MVC application. This example shows how to create a controller, a view, and pass data to the view.

### Create the Application

In the terminal, create a new ASP.NET MVC application with the following command:

```bash
dotnet new mvc -n MyApp
cd MyApp
```

### Controller

Add a new controller called `HomeController`:

```csharp
using Microsoft.AspNetCore.Mvc;
using MyApp.Models;

namespace MyApp.Controllers
{
    public class HomeController : Controller
    {
        public IActionResult Index()
        {
            var person = new Person
            {
                Name = "John",
                Age = 25
            };
            return View(person);
        }
    }
}
```

### View

Create a view called `Index.cshtml` that displays the data of a person:

```html
@model MyApp.Models.Person

<!DOCTYPE html>
<html>
<head>
    <title>Person Information</title>
</head>
<body>
    <h1>Name: @Model.Name</h1>
    <h2>Age: @Model.Age</h2>
</body>
</html>
```

### Run the Application

Run the application locally with the following command:

```bash
dotnet run
```

The application will be available at `http://localhost:5000`. When you visit the URL, you'll see the name and age of the person defined in the controller.

---

## Advanced ASP.NET Concepts

### Authentication

ASP.NET provides built-in support for user authentication, with features like cookie authentication and integration with external providers (such as Google or Facebook).

```csharp
public class AccountController : Controller
{
    public IActionResult Login()
    {
        // Login logic
        return View();
    }
}
```

You can configure authentication in `Startup.cs`:

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddAuthentication(CookieAuthenticationDefaults.AuthenticationScheme)
        .AddCookie(options => { options.LoginPath = "/Account/Login"; });
}
```

### Middleware

Middleware in ASP.NET is a way to intercept and process HTTP requests. You can add middleware to handle requests before or after the controller executes.

```csharp
public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
{
    app.UseMiddleware<MyMiddleware>();
    app.UseRouting();
    app.UseEndpoints(endpoints => { endpoints.MapControllers(); });
}
```

### RESTful APIs

ASP.NET is widely used to create RESTful APIs. You can create an API controller to serve data in JSON format.

```csharp
[Route("api/[controller]")]
[ApiController]
public class ProductsController : ControllerBase
{
    private static List<Product> _products = new List<Product>
    {
        new Product { Id = 1, Name = "Product A", Price = 10.0 },
        new Product { Id = 2, Name = "Product B", Price = 20.0 }
    };

    [HttpGet]
    public IEnumerable<Product> Get()
    {
        return _products;
    }
}
```

### API Consumption

You can consume APIs in your ASP.NET application using `HttpClient`.

```csharp
using System.Net.Http;
using System.Threading.Tasks;

public class ProductService
{
    private readonly HttpClient _httpClient;

    public ProductService(HttpClient httpClient)
    {
        _httpClient = httpClient;
    }

    public async Task<IEnumerable<Product>> GetProductsAsync()
    {
        var response = await _httpClient.GetStringAsync("https://api.example.com/products");
        return JsonSerializer.Deserialize<IEnumerable<Product>>(response);
    }
}
```
