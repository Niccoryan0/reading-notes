# Day 11 Readings


## Intro to EJS Series
- In the tutorial he uses app.set to create a path for the views folder. He also sets his "view engine" to EJS (Embedded JavaScript Rendering), and uses an index.ejs to render the header Hello World from index.ejs. I'm a bit unclear on how that all works still though.
- Within the render function that is pulled from index.ejs, he creates an object with a key-value pair for "foo" which he then places in index.ejs inside of some fancy brackets like so: <%= foo %> which prints the value, bar to the page. This can be used to insert text, assign image sources or href links.
- Additionally, loops and methods can be used within the brackets in order to do things like create list items for every item of an array or anything similar.
- If/else statements can also be written into EJS in order to add logic gates to the rendering.
- It is also shown that a "layout" can be applied to all pages, for things like making one header persistent across the website.
- Partial is used to pull data from a different EJS file and render it to the original file as well, with a use case for things like nav bars and such.