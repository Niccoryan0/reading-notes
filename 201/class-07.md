# Day 07 Readings
*Readings for day 7 of class*

## Article:
### Domain Modeling
Domain modeling refers to the process of creating a conceptual model in code for a specfic problem. When modeling on entity that'll have many instances, building self-containe dobjects with the same attributes and behaviors is helpful. Model it's attributes with a constructor funciton, and it's behavior with methods that each do one job well. Use the new keyword to create instances of the object. Store these objects in a variable so it's properties and methods can be accessed. Finally, use this variable within methods to make things easier. 

## HTML&CSS book:
### Chapter 6: “Tables” (pp.126-145)
Tables in HTML are drawn out row by row individually, they are created with a tr tag. The number of cells in a row is represented by the td element or th is it's the header. Rowspan and colspan are attibutes that can make cells span more than one row. Longer tables cna be split in a head, thead, a body, tbody and a foot, tfoot. 

## JS/JQuery Book:
### Chapter 3: “Functions, Methods, and Objects” (pp.106-144)
Creating objects can be done two different ways, with literal notation and with constructor notation. Literal notation is the normal, where you define one object and hard code it's attributes and methods specfically. Constructor notation, however, builds a template object that will be used to create other new objects of the same *class*, so if you have multiple of the same kind of object, wiht the same keys for properties but different values. Once you have a constructor, the new keyword can easily create new instances where you input the class's attributes. Aside from the DOM, there are two other sets of built-in objects, those being the Browser Object Model, which creates a model of the browser tab or window where the topmost object is the window object itself, the other is the Global JavaScript Objects which fo not form a single model but a group of individual objects that relate to parts of the language. These include things like strings, numbers and booleans which are JavaScript's native data types. The new Date(); command can retrieve the current date and time to use for things like clocks or keeping track of time for certian processes. 
