# 401-01 Readings

## Debugging for absolute beginners
- Ask questions like: "What did I expect my code to do? What happened instead?"
- Examine any assumptions about a result, hidden/unknown assumptions can lead to difficulties identifying the problem, i.e. am I using the right API/using it correctly, simple typos being overlooked, changes to code elsewhere in the program,object/variable values being unexpected, and overall intent of the code.
- Visual Studio offers lots of great debugging tools including breakpoints and the ability to step through the code in debug mode and monitor the values and states of everything in the code at each step.

## Try/Catch Blocks
- Using try and catch statements allows errors to be handled should they arise so that the program doesnt crash.

## Exception Handling
- C# has the following exception handling statements: throw (used to find an error), try-catch (used to catch individual errors), try-finally (finally will always be run even with errors), and try-catch-finally.

## C# 7.0 in a Nutshell - pg. 158 - 166 (start @ “try Statements and Exceptions)
- Catch blocks have access to an Exception object containing info on the error, they can either compensate for the error or rethrow the exception if you just need to log it. 
- Catch clauses specify which type of error a block should be catching, i.e. IndexOutOfRangeException or FormatException, catching System.Exception catches all possible errors.
- Exception filters, or when statements in a catch, to filter the exception futher to more specific cases.
- Finally statements can be used to run code after either the try or catch finished, sometimes called "clean up code".
- Unmanaged resources have a method called Dispose attached to them to clean them up, the using statement is a shorthand way to call dispose in a finally block.
- Throw statements can be used to display and identify errors in the code, and can be captured and rethrown as well, this is used to log an error without "swallowing" it, or can be used to rethrow more specific errors within the catch block.
- Key properties of System.Exception: StackTrace(string representing all methods called from origin of exception to catch block), Message (string w/ error desc.), InnerException (inner exception (if any) that caused the outer, which may have more inner exceptions)
- Common exception types (System.) : ArgumentException, ArgumentNullException, ArgumentOutOfRangeException, InvalidOperationException, NotSupportedException, NotImplementedException, ObjectDisposedException.

## Therac-25
- Computer-controlled radioation therapy machine that, due to programming errors, occasionally gave patients hundreds of times the normal amount of radation resulting in at least 6 serious injuries/deaths.
- "the overconfidence of the engineers and lack of proper due diligence to resolve reported software bugs are highlighted as an extreme case where the engineers' overconfidence in their initial work and failure to believe the end users' claims caused drastic repercussions."
- It was more an overall problem with poor software design and development practices than a specific error that caused it, specifically that it was designed in such a way that is was "realistically impossible to test in a clean automated way".

## Ariane 5
- A "heavy-lift space launch vehincle" used to deliver payloads to GTO or LEO. 
- The first launch of the rocket in 1996 failed and self-destructed 37 seconds after launch, caused by a data conversion from a 64-bit floating point value to a 16-bit signed integer value that represented horizontal bias. 
- The code was originally written for the previous Ariane 4 where three variables, including the horizontal bias variable, were "left unprotected because it was thought that they were 'physically limted or that there was a large margin of safety'".