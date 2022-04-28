# Identity

ASP.NET Core Identity is a fully featured membership system for creating and maintaining user logins. Using Identity API, you can sign in & sign out users, reset their passwords , lockout users & Implement Multi Factor Authentication. It can also integrate with the external login providers like Microsoft Account, Facebook, Google, etc.

When we create a new application, we can install the ASP.NET Core identity by choosing the Individual Accounts under the Authentication Type Option. Most of the Identity related services and UI forms like Register, Login & Logout are automatically created for us.


The Two important Identity services are User Manager and Sign In Manager.

## User Manager 
The UserManager is a concrete class that manages the user. This Class Creates, Updates, and Deletes the Users. It has methods to find a user by User ID, User Name, and email. UserManager also provides the functionality for adding Claims, removing Claims, add and removing roles, etc. It also generates password hash, Validates Users etc.

## Sign In Manager
SignInManager is a concrete class which handles the user sign in from the application.

The SignInManager is responsible for Authenticating a user, i .e  signing in and signing out a user. It issues the authentication cookie to the user. 

## Installing Identity API
Next step is to install the Identity API.
```
Install-Package Microsoft.AspNetCore.Identity
```

We will be using Entity Framework Core with Identity. Hence we need to install Identity EF Core Package.
```
Install-Package Microsoft.AspNetCore.Identity.EntityFrameworkCore
```

SQL Server is going to be our database.
```
Install-package Microsoft.EntityFrameworkCore.SqlServer
```

Need EF Core Tools to generate EF Core Migrations
```
Install-Package Microsoft.EntityFrameworkCore.Tools
```

## Identity Models
```
1. IdentityRole
2. IdentityRoleClaim
3. IdentityUser
4. IdentityUserClaim
5. IdentityUserLogin
6. IdentityUserRole
7. IdentityUserToken
``` 

## **Note**

ASP.NET Core Identity API already implements IdentityDbContext class, which inherits from the DBContext class. It already includes the DbSet Properties for the Identity Models.

## Registering the DBContext in Startup
The ASP.NET core uses dependency injection framework, where you can simply ask for the required services in the constructor of the class.

```
 services.AddDbContext<ApplicationDbContext>(options =>
        options.UseSqlServer(
            Configuration.GetConnectionString("DefaultConnection")));
```

The AddDbContext expects us to provide the Type that we will use for Context class, which is ApplicationDbContext.
```
services.AddDbContext<ApplicationDbContext>
```
The ```options.UseSqlServer``` lets us use the SQL Server

The connection string is retrieved from the Configuration.
```
GetConnectionString(“DefaultConnection”)
```

## Registering the Identity Services
In the startup class, we also need to register the Identity related services. To do that we use the AddIdentity extension method

```
services.AddIdentity<IdentityUser, IdentityRole>(
        options => {
            options.SignIn.RequireConfirmedAccount = false;
 
            //Other options go here
        }
        )
    .AddEntityFrameworkStores<ApplicationDbContext>();
```
```AddIdentity``` method takes types used for User ```(IdentityUser)``` 
& Roles 
```(IdentityRole)```.

# Authorization 
Authorization in ASP.NET Core determines whether a user can access a particular route, controller, controller action, Resource, etc.

## What is Authorization
Authorization is the process, which determines what the user can do or cannot do.

## Authentication Recap
Authorization depends on Authentication to identify the user.

In ASP.NET Core we add the Authentication to Middleware pipeline using the UseAuthentication method.
```
app.UseAuthentication();
app.UseAuthorization();
```

We usually add it after the ```UseRouting```, so that the authentication middleware knows about the URL being accessed by the User.

The purpose of the ***Authentication Middleware*** is to update the ```HttpContext.User``` Property with the information about the user 
```( ClaimsPrincipal )```.
 The ClaimsPrincipal contains the claims of the users.

All the middleware, which needs to know who the User is (For Example Authorization middleware) must come after the ```UseAuthentication```

The Authorization Middleware reads the ```ClaimsPrincipal``` from ```HttpContext.User``` and uses it to check whether the user is authorized.

## Authorization Strategies

1. **Declarative Authorization**
In this mode, we use the Authorize attribute to secure a page. The Authorize attribute describes how the page needs to be secured. The Authorization Middleware will read the attribute and figures out how to secure the page.

We can configure the Declarative Authorization using the following ways:
1. Simple Authorization
2. Claim based Authorization
3. Role based Authorization
4. Policy based Authorization.

---

2. **Imperative Authorization**
The Authorization middleware, which uses the Authorize attribute to check for permissions runs it much before the execution of the page handler or the action method.