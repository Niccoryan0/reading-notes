# 401-14 Readings

[Routing within MVC](https://docs.microsoft.com/en-us/aspnet/mvc/overview/older-versions-1/controllers-and-routing/asp-net-mvc-routing-overview-cs)

- ASP.NET Routing is enabled within the Web configuration file (Web.config) and there are four sections: "the system.web.httpModules section, the system.web.httpHandlers section, the system.webserver.modules section, and the system.webserver.handlers section".
- Route tables are created in the Global.asax file which is a special file that contains event handlers for the ASP.NET app lifecycle events. They're created during the Application Start event.
- Application_Start() calls RegisterRoutes() which creates the route table, a default table consists of a single route named Default which maps the first segment of a URL to a controller name, second segment to an action and third to a parameter named *id*.
- "The Default route includes defaults for all three parameters. If you don't supply a controller, then the controller parameter defaults to the value Home. If you don't supply an action, the action parameter defaults to the value Index. Finally, if you don't supply an id, the id parameter defaults to an empty string."


[Routing within Core](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/routing?view=aspnetcore-3.1)

- MapGet is used to define an endpoint, which is something that can be selected by matching the URL and HTTP method or executed by running the delegate. They are configured in UseEndpoints
- Endpoints can contain metadeta such as authorization policies, the metadata can be processed by routing-aware middleware and can be of any .NET type.
- An ASP.NET Core endpoint is:
  - Executable: Has a RequestDelegate.
  - Extensible: Has a Metadata collection.
  - Selectable: Optionally, has routing information.
  - Enumerable: The collection of endpoints can be listed by retrieving the EndpointDataSource from DI.