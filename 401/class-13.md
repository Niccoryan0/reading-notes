# 401-13 Readings

[Dependency Injection](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/dependency-injection?view=aspnetcore-3.1)

- A depedency is any object that another object requires (it *depends* on it). These are problematic and should be avoided as they require extra revision when making changes, they also must configured which becomes scattered across larger apps, and they're difficult to unit test.
- Dependency Injection addresses this via use of an interface or base class to abstract the dependency implementation, registration of the dependency in a service container built-in to ASP.NET Core, and injection of the service into the constructor of the class it'us used in.

[Repository Pattern](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/repository-pattern?view=aspnetcore-2.1)


[Repository Design Pattern](https://medium.com/@pererikbergman/repository-design-pattern-e28c0f3e4a30)
- Repository pattern follows SOLID Principles, and has two purposes according to this author: "first it is an abstraction of the data layer and second it is a way of centralising the handling of the domain objects."
- DAOs can get really big when working with large data tables, and can become clumsy and hard to modify, maintain and reuse. Repository Design Pattern breaks these large DAOs up into smaller more easy managed DAOs.

[SOLID Principles](https://www.telerik.com/blogs/30-days-of-tdd-day-five-make-your-code-solid)
*Images taken from SOLID Principles in Pictures below*

- Single Responsibility Principle - Each method or class should "have exactly one reason to change", essentially they should each have just one job or responsibility.

![Single Responsibility Principle](https://miro.medium.com/max/1000/1*P3oONz9Da3Tc1w97fMV73Q.png)

- Open/Close Priniciple - Similar to Encapsulation and Inheritance, unifies them in a sense. It says software should be open for extension and closed to modification.

![Open/Close Priniciple](https://miro.medium.com/max/1000/1*0MtFBmm6L2WVM04qCJOZPQ.png)

- Liskov Substitution Principle - An object in the application should be able to replaced with a type derived from it without breaking the application.

![Liskov Substitution Principle](https://miro.medium.com/max/992/1*2hmyR9L43Vm64MYxj4Y89w.png)

- Interface Segregation Principle - Clients shouldn't be forced into relying on interfaces they don't use, i.e. make "fine-grained" interfaces so that they can tackle specific problems.

![Interface Segregation Principle](https://miro.medium.com/max/992/1*2hmyR9L43Vm64MYxj4Y89w.png)

- Dependency Inversion Principle - Make couple as loose as possible, DIP is the idea that code shuld depend on abstractions not concrete implementations.

![Dependency Inversion Principle](https://miro.medium.com/max/1000/1*Qk8tDmjQlyvwKxNTfXIo0Q.png)

[Why SOLID Matters](https://www.telerik.com/blogs/why-solid-matters)
- Examples and explanations for why and how the SOLID principles should be applied.

[SOLID Principles in Pictures](https://medium.com/backticks-tildes/the-s-o-l-i-d-principles-in-pictures-b34ce2f1e898)
