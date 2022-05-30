# MVC Forms

## View Model
A view is used to display data using the model class object. The Views folder contains all the view files in the ASP.NET MVC application.

A controller can have one or more action methods, and each action method can return a different view. In short, a controller can render one or more views. So, for easy maintenance, the MVC framework requires a separate sub-folder for each controller with the same name as a controller, under the Views folder.

## Razor View Engine
Microsoft introduced the razor view engine to compile a view with a mix of HTML tags and server-side code. The special syntax for razor view maximizes the speed of writing code by minimizing the number of characters and keystrokes required when writing a view.

The razor view uses @ character to include the server-side code instead of the traditional <% %> of ASP. You can use C# or Visual Basic syntax to write server-side code inside the razor view.

ASP.NET MVC supports the following types of razor view files:

**.cshtml** => C# Razor view. Supports C# code with html tags.

**.vbhtml** => Visual Basic Razor view. Supports Visual Basic code with html tags.

**.aspx** => ASP.Net web form

**.ascx** => ASP.NET web control

## Creating a View
You can create a view for an action method directly from it by right clicking inside an action method and select Add View

## Form In ASP.NET MVC
 How to create Forms in ASP.NET MVC? 
 1.  Weakly Typed (Synchronous)
 Advantage and Disadvantage of Weakly Typed Form

**Advantage:**
1. It is easy to create a form using Weakly Typed mechanism
2. Mostly used when you need to create a form with one or two input items.

**Disadvantage:**
1. Because, it is not strongly typed so IntelliSense doesn't help you.
2. Have higher chance of getting exception and runtime error messages.
3. Very difficult to manage when forms have multiple input items and controls.
4. It is very clumsy when you need to add or remove some input items.
 
 2. Strongly Typed (Synchronous)
 3. Strongly Typed AJAX (Asynchronous)
 4. HTML, AJAX and JQUERY


