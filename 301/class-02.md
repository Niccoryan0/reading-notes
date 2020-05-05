# Day 2 readings
*Readings for class # 2*

## JavaScript and jQuery book by Jon Duckett pages: 
### 293-301 
jQuery allows us to target elements using CSS-style selectors and perform certain actions them using jQuery methods. $() is used for all jQuery methods, the alternative is jQuery() but the $ is much easier. It's similar to DOM manipulation in that it performs similar tasks, can store jQ objects in variables, and because it manipulates the DOM in much the same way. It's different in that it doesn't require fallback code (being cross-browser), it's much simpler to select elements and handle events, loops aren't necessary to affect multiple elements, additional tasks can be accomplished such as animation, and once an element is selected muliple methods can be applied to it.
### 306-331  
When one or more objects is selected, a jQ object is returned, called a matched set or jQuery selection. jQuery can be used to both get and set any information from html elements, such as their text content, value, properties, etc. and can then set those values to something different. jQuery does not create copies of the elements though, it simply holds a reference to them to access them. Storing these elements or any jQuery as a variable is called caching it. The .ready() function is commonly used tomakesure a page fully loads before any code is run. 
### 354-357
Additionally to hosting the jQuery file within your own website you can use a link to a CDN that hosts jQuery, but a fallback version should still be included. When this was written, Max CDN, Google and Microsoft offered jQuery through their CDN. 

## 6 Reasons for Pair Programming
Basics: Having two programmers working together, one acting as the Driver, managing the “mechanics” of the code i.e. being the one on the computer acting and typing, and the Navigator who watches and thinks about the big picture and other more abstract questions.

Why do it?: It helps to build the very important skills necessary to learning a new language of any kind, listening, spekaing, reading and writing. Research has also shown that while it takes slightly longer to have two people work together like this, the code is higher-quality and requires less effort later fixing it. It allows programmers to engage and focus more, learn to ask for and receive help, and observe different approaches to problem-solving. It also helps to prepare for job interviews and the work environment, because many corporations use it in practice and in interviews.