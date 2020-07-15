# 401-08 Readings

## Collections
- Collections are essentially flexible arrays, they are able to work with groups of objects where the size of the collection can grow and shrink dynamically unlike arrays. A collection initializer can instantiate a collection if the contents are known in advance. 
- Foreach loops cannot be used in normal colections, but a regular for loop can. 
- Some common collection classes include: System.Collections.Generic classes, System.Collections.Concurrent classes and System.Collections classes.
- Some common generic classes are: Dictionary, List, Queue, SortedList and Stack.
- Concurrent classes provide efficient, thread-safe operations for accesstion items from multiple threads. They should be used wherever multiple threads are concurrently acdcessing the collection. Examples including BlockingCollection, ConcurrentDictionary, ConcurrentQueue, and ConcurrentStack.
- System.Collections classes do not store elements are specifically types but instead as type Object. These are legacy types and should be avoided whenever possible, but some examples include ArrayList, Hashtable, Queue and Stack.

## Enumerations Types
- Enumeration types are "value types defined by a set of named constants of the underlying integral numeric type." The default values are of type int if not specified, starting at 0 and increasing. 
- System.Enum is the abstract base class of all enumeration types, providing methods to get info aout enumeration type and it's values.
- For any enum type there are explicit conversions between enum type and underlying integral type casting an enum value to it's underlying type will result in the associated integral value being given.