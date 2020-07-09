# 401-04 Readings

## Classes
[Link](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/classes)\
- "A type that is defined as a class is a reference type."
- When new objects are created, memory is allocated on the managed heap for the specific object, while the varible is only a reference to it's location. 
- "Types on the managed heap require overhead both when they are allocated and when they are reclaimed by the automatic memory management functionality of the CLR, which is known as garbage collection. However, garbage collection is also highly optimized and in most scenarios, it does not create a performance issue."
- Classes are declared with the use of the class keyword followed by a unique identifier i.e. public class Customer{}.
- Classes defines types of objects but are not objects themselves. Classes are like blueprints, objects are the actual building and can be called an "instance of a class".
- Class inheritance means that when a class is created it can inherit from any other interface or class not defined as sealed, and it can be inherited from. This is done via derivation, which is expressed as BaseClass : DerivedClass, only one base class can be used, but because base classes can also have their own inheritance they can indirectly inherit multiple base classes. A class can also "directly implement more than one interface".
- Classes declared abstract contain abstract methods with a signature definition but no implementation, and they can't be instantiated, only used through derived classes that implement their methods. Sealed classes do no allow other classes to derive form them.


## Constructors
[Link](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/constructors)\
- If a constructor is not provided for a class C# will create one that instantiates an object sand sets member variables to defaults. 
- "A constructor is a method whose name is the same as the name of its type. Its method signature includes only the method name and its parameter list; it does not include a return type."
- Single statement constructors can be replaced with express body definition (arrow function).
- Instance constructors create a new object, but classes or structs can also have static constructors, which initialize static members of the type and are parameterless. If you don't provide a static constructor to initialize static fields the compiler initializes static fields to defaults.

## Properties
[Link](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/properties)\
- Properties allow a class's values to be gotten and set publicly while hiding their implementation or verification code. Get and set are the keywords used, value is used to set values as well.
- "Properties can be read-write (they have both a get and a set accessor), read-only (they have a get accessor but no set accessor), or write-only (they have a set accessor, but no get accessor). Write-only properties are rare and are most commonly used to restrict access to sensitive data."
-"Simple properties that require no custom accessor code can be implemented either as expression body definitions or as auto-implemented properties."
- Properties that only need to assign or retrieve a variable can be simplified with auto-implemented properties, where you can simple write get; set; in curly braces to establish either of them.

## Stack and Heap
[Link](https://www.c-sharpcorner.com/article/C-Sharp-heaping-vs-stacking-in-net-part-i/)\
- The stack is in charge of what is getting executed when, and like a stack of boxes, whatever goes on last has to come off first, First In Last Out. The stack is self maintaining, it takes care of it's own memory management, discarding items as they're executed.
- The heap is generally just in charge of holding information, which can be accessed at any time unlike the stack, similar to a heap of laundry on the bed where any article of clothing can be pulled out at will. The heap must worry about Garbage Collection (GC), which deals with "keeping the heap clean".
- For main things are put into the stack and heap during execution of code: Value Types, Reference Types (class, interface, delegate, object, string), Pointers (Reference to a type, managed by CLR), and Instructions. 
- 

## Garbage Collection Fundamentals
[Link](https://docs.microsoft.com/en-us/dotnet/standard/garbage-collection/fundamentals)\
