# 401-32 Readings

## Intro to View Components
[Link](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/view-components?view=aspnetcore-2.1)
- View components are like partials but are far more powerful, and can be used with both MVC and Razor Pages.
- Can be created by deriving from the ViewComponent class, decorating a class with the ViewComponent attribute or deriving from a class with the attribute, or creating a class where the name ends with the soffic ViewComponent
- Logic is defined in a InvokeAsync method that returns a Task<IViewComponentResult> or a sync Invoke method. They typically initialize a model and pass it to the view by the calling the View method.
- View components can also be invoked via Tag Helpers in ASP.NET core 1.1+, this is done by assigning the method to a specific helper.
- Each parameter in a view component is a required attribute. See this GitHub issue. If any parameter is omitted:
  - The InvokeAsync method signature won't match, therefore the method won't execute.
  - The ViewComponent won't render any markup.
  - No errors will be thrown.

## View Components
[Link](https://mariusschulz.com/articles/view-components-in-asp-net-core-mvc)
- This is a second reference that summarizes most of the information above, use as a reference for Views it's much better laid out than the docs.