# Routing and Navigation 

A route is a URL pattern. Routing is a pattern matching process that monitors the requests and determines what to do with each request. In other words we can say Routing is a mechanism for mapping requests within our MVC application. The Routing mechanism passes the request to the handler. A handler may be a physical path such as .aspx or may be a class capable of processing our request such as controller in MVC.

## What is Routing 
Routing means showing a way. ASP.NET MVC Routing does the same thing; it shows the way to a request. Basically, routing is used for handling HTTP requests and searching matching action methods, and then executing the same.

* It constructs outgoing URLs that correspond to controller actions.
* Routing the map request with Controller’s Action Method.

We can call Routing a pattern matching technique which manages the incoming request. It matches the request with Route Table.

## Why Routing is required
In MVC, Model View Controller are the main independent components. These three components work individually and all-together at the same time.
 
Any incoming request is handled by Controller. MVC is not mapped directly with physical UI output file. That is mapped by Controller at run time and route table.

## Advantages of Routing

1. Routing is very friendly & helpful for SEO (Search Engine Optimization)
2. All URLs are not directly mapped with physical file.
3. More powerful securities than in WebForm.

***To learn more*** [Routing](https://www.c-sharpcorner.com/article/learn-about-asp-net-mvc-routing/)

## Navigation 

navigation in a web application is very important to understand since practically several times in a web application project we need to navigate from one page to another and return to the page of the original page as part of the functionality.

## Processing
When processing the client request when a web server encounters the code block response.redirect with the location URL to be redirected it will send back a response header to the client then the client initiates a get request of the new page.

## Important Sticky
* It redirects to a new redirected URL where it is redirected in the browser.
* It maintains the history and previous page is available with the back button.
* It redirects the user to a web page hosted on the same server or a different server.
* It has an additional round trip to the server that makes it a bit slower.

***To learn more*** [Navigation](https://www.c-sharpcorner.com/UploadFile/de41d6/navigation-techniques-in-Asp-Net/)