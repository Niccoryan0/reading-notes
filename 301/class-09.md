# Day 9 Readings

## Functional Programming Concepts
- Functional programming is a paradigm or structure in programming that "treats computation as the evaluation of mathemathical functions and avoids changing-state and mutable data".
- Pure Functions: Functions are considered pure if it returns the same results given the same arguments, known as being deteministic, and if it does not cause any noticeable side effects. They also must not use global objects or variables that are not passed in as parameters. Things like reading files and generating random numbers will make a function inherently impure. 
- On the side effects end of things, if a function modifies a global variable like a counter, it is impure. This is because mutability of objects is discouraged in function programming.
- To achieve things like iteration while maintaining immutability, recursion is often used. 
- Memoization (the ability to store the results of expensive function calls and return cached data to cut down on run time) is also possible with pure functions, since the output is always the same if given the same parameters.
- Functions are also treated as "first-class entities" in Functional PRogramming meaning they can be referred to by constants and variables, pass it as a parameter to other function and return is as a result of other functions. Essentially treating functions as values and use them like data. 
- Some higher order functions covered: 
    - Filter
    - Map
    - Reduce * 

## Refactoring JS For Readability
- Lots of improvements to JS readability can be made. 
- In the first example, it is shown that iterating over a flat array many times is not efficient or best practice, the option they show is to convert the array to a "new Map()".
- The second example shows the author simplifying a few function definitions but combining two similar ones into one with a template literal to apply any differences between the two uses.
- The author then gives the following advice:
    - Return early from functions
    - Cache variables so functions can be read like sentences:
    - Check for Web APIs before implementing your own functionality:
