# Class 03 Readings
*Readings for Fay 3 of class*

## HTML&CSS:
### Chapter 3: “Lists” (pp.62-73)
Ordered Lists
: Numbered

Unordered Lists
: Bulleted

Definition
: Used to define terminology, no numbers or bullets

*Lists can be nested inside one another*
### Chapter 13: “Boxes” (pp.300-329)
*For each HTML element "box", CSS can control:* the dimensions of the box (setting or limiting width and height), the boxe's borders (including type, size, color, and shape), margins (space between border and other boxes), padding (space between border and boxe's content), and where the box is located on the page. Additionally, CSS can control whether it's an inline or block element and it's visibility on the page.

## JS/JQuery:
### Chapter 4: “Decisions and Loops” from switch statements on (pp.162-182)
Switch statements
: Essentially a shorthand for writing long if...else statements, all of the if...else cases are written together in one function with the method switch(variable to check) at the top and any possible cases laid out inside ending in a break statement that will return it to the rest of the code. It's faster than writing a bunch of if...else statements and runs faster at it stops after a match is found while if...else will always run all the way through.

Truthy and falsy
: Every value in JavaScript can be thought of as either truth or false. Falsy values, values JavaScript treats as value, include boolean false, the number 0, empty strings, NaN, and empty variables. Just about everything else will evaluate to truth, any number other than one, any string with something in it, etc.. This is why we use the strict equality operators in JavaScript, i.e. ===, !==, because with regular equality operators more unexpected results may happen such as false == 0 resulting in true because both are falsy values.

Short Circuit Values
: Logical operators process left to right and stop when they reach a result, so using something like an or operator in a variable assignment or if statement will check the first value and only continue to each subsequent value if the one it's on is false or undefined. 

Loops
: Loops will run a block of code repeatedly until the condition it is checking returns false. Three common types of loops in JavaScript are **for** loops, which will run a code a specific number of times, **while** loops, which are better if you aren't sure how many times it needs to run as it will simply go for as long as the condition given is true, and **do...while** loops which are the same as while loops except the key fact that it will always run atleast once, whereas a while loop won't run at all if the first check it does returns false. 

Loop counter
: For loops require a counter as a condition, so that it knows how long to run, which consists of an initialization of a variable, often a placeholder like i that will only be used in the loop, as well as a condition that needs to be met and an update to the variable such as i++ (adds one to i every iteration)