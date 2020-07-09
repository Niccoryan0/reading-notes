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
- "A Reference Type always goes on the Heap easy enough, right? Value Types and Pointers always go where they were declared.  This is a little more complex and needs a bit more understanding of how the Stack works to figure out where "things" are declared."
- "Now, Value Types are also sometimes placed on the Heap.  Remember the rule, Value Types always go where they were declared?  Well, if a Value Type is declared outside of a method, but inside a Reference Type, it will be placed within the Reference Type on the Heap."

## Garbage Collection Fundamentals
[Link](https://docs.microsoft.com/en-us/dotnet/standard/garbage-collection/fundamentals)\
- The GC frees devs from manually releasing memory, efficiently allocates heap objects, reclaims unused objects and clears their memory, and provides memory safety by ensuring objects can't use other object's content.
- Free memory has no references to it and is available for allocation, Reserved memory is available for use but can't be used for any other allocation requests, it cannot store data until it is committed, and Committed memory is assigned to physical storage.
- The GC's optimizing engine performs colections at the determined best time and releases memory for objects no longer in use, which it finds by examining the app's roots (static fields, local vars and parameters).
- Conditions for DC: system has low physical memory, memory used by allocated objects on the managed heap passes a certain threshold, or GC.Collect is called, but this is almost never necessary.
- A "managed heap" is what the GC creates by allocating memory to store and manage objects. 
- In reclaiming, live objects are compacted and can be moved together while dead space is removed, shrinking the heap.

- The GC algorithm is based on several considerations:
1. "It's faster to compact the memory for a portion of the managed heap than for the entire managed heap.
2. Newer objects have shorter lifetimes and  older objects have longer lifetimes.
3. Newer objects tend to be related to each other and accessed by the application around the same time."
