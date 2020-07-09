# Prework readings

## History
- C# started in the shadow of Java, aiming to be a "simple, modern, general-purpose OO language". Version 3 was the first big ground-breaking update for C# and .NET, with the killer feature being Language-Intergrated Query (LINQ), starting it's change into a hybrid OO/Functional language.

## Tooling
- Visual Studio provides some very helpful built in debugging tools, breakpoints can be used and given conditionals easily, and the stepping functions allow for the code to be traversed much more efficiently it seems like.
- Managed Code is "code whose execution is managed by a runtime", which in this case is the Common Language Runtime or CLR regardless of which implementation is in use. CLR compiles and executes the code, "on top of that, runtime provides several important services such as automatic memory management, security boundaries, type safety etc". This reduces overhead for the developer in relation to unmagaged code such as that run in C/C++ prograns, where the program is a binary that the OS loads into it's memory and starts but everything else (memory management, security considerations, etc..) are on the programmer.
- Code written in high-level .NET languages (C#, Visual Basic, F#) compiles to what is called "Intermediate Code", and once that happens the CLR can take over and perform "Just-In-Time compiling, or JIT-ing", turning the IL, or Intermediate Language, into machine code. Other names for IL are Common Intermediate Language, CIL, or Microsoft Intermediate Language, MSIL.
- The CLR allows "passing the boundary between managed and unmanaged langauges" which is known as interoperability, or interop. This allows programmers to do things like wrap an unmanaged library and call into it. "However, it is important to note that once you do this, when the code passes the boundaries of the runtime, the actual management of the execution is again in the hand of unmanaged code, and thus falls under the same restrictions." C# also allows use of unmanaged constructs such as the ability to utilize unsage context to leave pieces of code unmanaged by the CLR.
- "[Managed Code] benefits from features such as cross-language integration, cross-language exception handling, enhanced security, versioning and deployment support, a simplified model for component interaction, and debugging and profiling services."
- 

## Language
