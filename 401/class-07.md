# 401-07 Readings

## Inheritance
- Inheritance describes the ability to reuse, extend and modify behavior defined in other classes by allowing any class to inherit the properties and methods of another.
- When a class derives from another, the derived class implicitly receives all members of the base class except constructors and finalizers. 
- Methods declared as virtual, derived classes can override the method with a different implementation, and for abstract base classes that method must be overridden in a non-abstract class if directly inheriting from it. If the derived class is also abstract it inherits the abstract members with implementing them.
- "An interface is a reference type that defines a set of numbers." They're used to define specific abilities for classes that might lack an is-a relationship.

## Abstraction 
- Abstract classes cannot be instantiated, they exist to create a comon definition that will derived by multiple other classes. They can define methods but abstract methods have no implementation until the method is overriden by a concrete class.
- "If a virtual method is declared abstract, it is still virtual to any class inheriting from the abstract class."
- Classes can be sealed so that they aren't able to be used as a base class.

## Polymorphism
- Meaning "many shapes", polymorphism is the principle that allows derived classes to override and change the inherited information from base classes. 
- "The derived class may override virtual members in the base class, defining new behavior."
- "The derived class inherit the closest base class method without overriding it, preserving the existing behavior but enabling further derived classes to override the method."
- "The derived class may define new non-virtual implementation of those members that hide the base class implementations."


## OOP Principles
- Classes can have class members that include properties that describe data about the class, methods for class behavior, and events that proviede communication between seperate objects and classes.
- Finalizers are used to destruct instances of a class, a task usually done by the GC but if resources are unmanaged a finalizer will clean up the application.
- Events allow communication between objects and classes to know when an event has occured. The *publisher* is the class that sends/raises the event and the receiving class is called the *subscriber*.
- Nested classes are private by default.
- The follow access modifiers are available: public, private, protected, internal, protected internal and private protected, they all define how visible the guts of a class or method.
- Static members of a class are properties, procedures or fields shared by all instances of the class.
- Anonymous types allow us to create objects without writing a class definition for the data type, the compiler will generate the class for us w/ no usuable name and containing the properties you specify when declaring the object.
- Interfaces are like classes in that they define a set of props, methods,m and events but they do not provide any implementation and are implemented by classes.
- Generics: "Classes, structures, interfaces, and methods in .NET can include type parameters that define types of objects that they can store or use. The most common example of generics is a collection, where you can specify the type of objects to be stored in a collection."
- Delegates are a type that defines a method signatures and can provide reference to any method with a compatible signature, they are used to pass methods as arguments to other methods.