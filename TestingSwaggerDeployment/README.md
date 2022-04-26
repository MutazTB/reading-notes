# Swagger 

**What is SwaggerUI**
 
Swagger-UI is an open source tool to generate the documentation for our Api project based on specification. Here we can able to configure the input and output for our Api’s and its very convenient to use instead of Postman.

**Adding Swagger**
* To add Swagger to our application we need to install Swashbuckle.AspNetCore package from Nuget package manager.

* Add the below set of lines in Startup.cs file for Api versioning and swagger api endpoint configuration.

```
services.AddSwaggerGen(c =>
{
    c.SwaggerDoc("v1", new OpenApiInfo 
    { Title = "The API", 
    Version = "v1" }
    );
});
```
```
// Enable middleware to serve generated Swagger as a JSON endpoint.  
      app.UseSwagger();  
  
      // Enable middleware to serve swagger-ui (HTML, JS, CSS, etc.), specifying the Swagger JSON endpoint.  
      app.UseSwaggerUI(c =>  
      {  
        c.SwaggerEndpoint("/swagger/v1/swagger.json", "My API V1");  
      });  
```

* Change the launch Url in launchSettings.json (swagger/index.html is default url for swagger-UI documentation)

---

# Testing Controllers

**Why Test Controllers**
Controllers are a central part of any ASP.NET Core MVC application. As such, you should have confidence they behave as intended for your app. Automated tests can provide you with this confidence and can detect errors before they reach production. It’s important to avoid placing unnecessary responsibilities within your controllers and ensure your tests focus only on controller responsibilities.

Typical controller responsibilities:

* Verify ModelState.IsValid
* Return an error response if ModelState is invalid
* Retrieve a business entity from persistence
* Perform an action on the business entity
* Save the business entity to persistence
* Return an appropriate IActionResult

**Goals of Unit Testing**
The primary goal of unit testing is to take the smallest piece of testable software in the application and determine whether it behaves exactly as you expect. Each unit is tested separately before integrating them into modules to test the interfaces between modules.

***To learn more about =>*** [Testing Controllers](https://www.tutorialspoint.com/asp.net_mvc/asp.net_mvc_unit_testing.htm)