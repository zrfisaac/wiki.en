# ASP.NET MVC

---

### **Table of Contents**  
1. [Introduction to ASP.NET MVC](#introduction-to-aspnet-mvc)  
2. [Installing ASP.NET MVC](#installing-aspnet-mvc)  
3. [ASP.NET MVC File Structure](#aspnet-mvc-file-structure)  
4. [Routing in ASP.NET MVC](#routing-in-aspnet-mvc)  
5. [Controllers and Views](#controllers-and-views)  
6. [Database Configuration](#database-configuration)  
7. [Useful Commands](#useful-commands)  
8. [Additional Resources and Links](#additional-resources-and-links)  

---

### **Introduction to ASP.NET MVC**  

ASP.NET MVC is a web development framework that follows the Model-View-Controller (MVC) architectural pattern, developed by Microsoft. It allows you to create scalable and well-structured web applications by separating business logic, user interface, and flow control.  

---

### **Installing ASP.NET MVC**  

#### Requirements  
- Visual Studio (recommended for development)  
- .NET SDK (Software Development Kit)  
- .NET Core or .NET Framework (depending on the version you choose)  

#### Installation via Visual Studio  
1. Open Visual Studio and select "Create a new project".  
2. Choose the "ASP.NET Core Web Application" template and click "Next".  
3. Select the "Web Application (Model-View-Controller)" option to create an MVC project.  
4. Configure the project name and the location where it will be saved.  
5. Click "Create".  

#### Installation via .NET CLI  
If you prefer using the command line, run the following command to create a new MVC project:  
```bash
dotnet new mvc -n ProjectName
cd ProjectName
dotnet run
```

---

### **ASP.NET MVC File Structure**  

The file structure in ASP.NET MVC follows a pattern that simplifies development and project organization. Here are the main directories and files:  

- **`Controllers/`**  
  Contains the controllers, which manage requests and the application’s flow logic.  
  Example: `HomeController.cs`  

- **`Views/`**  
  Contains the views (web pages) that are rendered and sent to the user. Each controller can have an associated views folder.  
  Example: `Views/Home/Index.cshtml`  

- **`Models/`**  
  Contains model classes that represent application data and are used for manipulation and validation.  
  Example: `Product.cs`  

- **`wwwroot/`**  
  Contains static files such as CSS, JavaScript, and images that are served to the client.  

- **`appsettings.json`**  
  Application configuration file used to store settings, such as the database connection string.  

---

### **Routing in ASP.NET MVC**  

In ASP.NET MVC, routes are configured in the `Startup.cs` or `Program.cs` file (depending on the .NET version). The routing pattern can be adjusted for different needs.  

#### Default Route  
In the `Program.cs` (or `Startup.cs` in older versions) file, the default route configuration is generally as follows:  
```csharp
public class Program
{
    public static void Main(string[] args)
    {
        CreateHostBuilder(args).Build().Run();
    }

    public static IHostBuilder CreateHostBuilder(string[] args) =>
        Host.CreateDefaultBuilder(args)
            .ConfigureWebHostDefaults(webBuilder =>
            {
                webBuilder.UseStartup<Startup>();
            });
}
```

The default route is configured in the `Configure` method inside `Startup.cs`:
```csharp
public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
{
    if (env.IsDevelopment())
    {
        app.UseDeveloperExceptionPage();
    }
    else
    {
        app.UseExceptionHandler("/Home/Error");
        app.UseHsts();
    }

    app.UseHttpsRedirection();
    app.UseStaticFiles();

    app.UseRouting();

    app.UseEndpoints(endpoints =>
    {
        endpoints.MapControllerRoute(
            name: "default",
            pattern: "{controller=Home}/{action=Index}/{id?}");
    });
}
```

The above default route maps to `HomeController` and the `Index` method.

---

### **Controllers and Views**  

#### Creating a Controller  
In ASP.NET MVC, controllers are classes that manage request and response flow. To create a controller, create a class that inherits from `Controller`.

Example of a simple controller:
```csharp
public class HomeController : Controller
{
    public IActionResult Index()
    {
        return View();
    }

    public IActionResult About()
    {
        return View();
    }
}
```

#### Creating a View  
Views are files that define the HTML content displayed to the user. In ASP.NET MVC, views typically have the `.cshtml` extension.

Example of `Index.cshtml`:
```html
@{
    ViewData["Title"] = "Home Page";
}

<div class="text-center">
    <h1 class="display-4">@ViewData["Title"]</h1>
    <p>Welcome to ASP.NET Core MVC!</p>
</div>
```

#### Binding between Controller and View  
The `HomeController` with the `Index` action automatically renders the `Index.cshtml` view.  
When the user accesses the route `/Home/Index`, the `Index` method is called, and the result is the rendering of the `Index.cshtml` view.

---

### **Database Configuration**  

#### 1. Install Entity Framework Core  
Use NuGet or the .NET CLI to install the Entity Framework Core package.

Via CLI:  
```bash
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
```

#### 2. Configure the Connection String  
In the `appsettings.json` file, add the connection string for the database:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Database=MyDatabase;User Id=myusername;Password=mypassword;"
  }
}
```

#### 3. Create and Configure the Model  
Example of a `Product.cs` model:
```csharp
public class Product
{
    public int Id { get; set; }
    public string Name { get; set; }
    public decimal Price { get; set; }
}
```

#### 4. Create the Database Context  
Create an `ApplicationDbContext` class that inherits from `DbContext`:
```csharp
public class ApplicationDbContext : DbContext
{
    public DbSet<Product> Products { get; set; }

    public ApplicationDbContext(DbContextOptions<ApplicationDbContext> options) : base(options) { }
}
```

#### 5. Configure the Context in `Startup.cs`  
```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddDbContext<ApplicationDbContext>(options =>
        options.UseSqlServer(Configuration.GetConnectionString("DefaultConnection")));
    services.AddControllersWithViews();
}
```

---

### **Useful Commands**  

1. **Run the Project:**  
   ```bash
   dotnet run
   ```

2. **Create a New Controller:**  
   ```bash
   dotnet aspnet-codegenerator controller ControllerName --controller
   ```

3. **Generate Migrations (Database):**  
   ```bash
   dotnet ef migrations add InitialCreate
   ```

4. **Update the Database:**  
   ```bash
   dotnet ef database update
   ```
