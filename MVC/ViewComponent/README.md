# View Components

## What are View Components

View Component are powerful, self-contained, reusable UI components which can consistently generate reusable HTML from a razor view. They can generate both static and dynamic contents which can be customized further using parameters. View Components can also be used to connect backend databases or services to fetch data.

**important points to remember when implementing View Components**
1. View Components are suitable for rendering a chunk rather than a whole response. This makes them ideal for rending UI elements, widgets, dynamic menus, shopping cart, login page, sidebars etc.
2. View Components don’t support features like View Data or Data Binding and only depend on the data provided to them at runtime as parameters
3. View Components support separation of concern and testability benefits in a sense that they always generate consistent output no matter where they are used.
4. View components can be parameterized to customize the output, and they can also have their own business logic.

## View Components vs Partial Views 
They are designed to do everything that a Partial View was doing in previous versions of ASP.NET and more. When we use partial view, we still have dependency on controller, and we can access View Data and controller contents while in View Component we don’t even need a controller. View Components have their own separate class which can run some business logic and generate response using razor view. We can think View Components as mini controllers with less overhead than a full MVC Controller.

## Creating a View Component

**The view component class** 
A view component class can be created by any of the following:

* Deriving from ViewComponent
* Decorating a class with the [ViewComponent] attribute, or deriving from a class with the [ViewComponent] attribute
* Creating a class where the name ends with the suffix ViewComponent

**View component methods**
A view component defines its logic in an:

* InvokeAsync method that returns Task<IViewComponentResult>.
* Invoke synchronous method that returns an IViewComponentResult.

**View search path**
The runtime searches for the view in the following path:

* /Views/{Controller Name}/Components/{View Component Name}/{View Name}

## Invoke a view component
```
@await Component.InvokeAsync("Name of view component",
{Anonymous Type Containing Parameters})
```
## Invoke a view component as a Tag Helper
```
<div>
       Maxium Priority: @ViewData["maxPriority"] <br />
       Is Complete:  @ViewData["isDone"]
    @{
        int maxPriority = Convert.ToInt32(ViewData["maxPriority"]);
        bool isDone = Convert.ToBoolean(ViewData["isDone"]);
    }
    <vc:priority-list max-priority=maxPriority is-done=isDone>
    </vc:priority-list>
</div>
```

## Invoke a view component directly from a controller
```
public IActionResult IndexVC(int maxPriority = 2, bool isDone = false)
{
    return ViewComponent("PriorityList",
        new { 
           maxPriority = maxPriority,
           isDone = isDone
        });
}
```