# 401-28 Readings

## Layouts
[Link](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/layout?view=aspnetcore-2.1)

- Layouts can be used to define a top level template for views in an app, making pages render the same if they have the same layout. Thinks like headers, navs, footers and scripts/links can all be placed into a layout, which can simply call to render different body sections.

## Partial Views
[Link](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/partial?view=aspnetcore-2.1)

- Partials can be used to dry up repeated pieces of HTML code across multiple pages in an app.
- Partials are used to break up large files into smaller components, as well as reduce the duplication of common markup content across all HTML files.
- If an HTML helper is used, PartialAsync should be used as the synchronous versions can cause a deadlock.
- Special models can also be passed into partials when they are called.

## View Models
[Link](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/overview?view=aspnetcore-2.2)

- Views are used in MVC architecture and are attached to a controller. They can utilize layouts, partial views and view components.
- Using views, an app is easier to maintain as it's better organized, it is loosely coupled and the views can be built and updated seperately, it's easier to test the UI parts, and it reduces repeated sections of UI due to the better organization.
- Strongly typed data can be passed to views via a viewmodel, while weakly typed datas can be send in ViewData or the ViewBag.

## Tag Helpers References
[Tag Helpers](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/layout?view=aspnetcore-2.1)
[Tag Helpers with Forms](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/layout?view=aspnetcore-2.1)

- "Tag Helpers enable server-side code to participate in creating and rendering HTML elements in Razor files. For example, the built-in ImageTagHelper can append a version number to the image name." See links for references about how they can be used.