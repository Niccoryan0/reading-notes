# Reading 01

*Pre-work readings*

## HTML & CSS:
### Introduction (pp.2-11)
**Overview:**

*Web basics:* The content and general appearance of any website are primarily created using HTML (HyperText Markup Language) and CSS (Cascading Style Sheets). These work in tandem to create the front face of any website.  To connect to the internet we go through ISPs (Internet Service Providers), who take a domain that we are attempting to reach and connect us to a Domain Name System, or a network of different servers, to locate the domain's IP address and request the page being searched which is then sent back to your computer.

**Definitions:**

HTML
: Creates the content of the site such as words, images, tables, and more. Can be thought of as the Builder of a website.

CSS
: Gives the website it's presentation and layout, things like font styles and positions of different elements on the screen. Gives pretty much any and all style to plain old HTML, can be thought of as the Artist of a website.

DNS
: Domain Name System's act like directories full of IP addresses, connecting us to whichever we need to access a certain domain.

### HTML & CSS Chapter 1: “Structure” (pp.12-39)
**Overview:**

*Structure:* At their core, HTML webpages are just text documents, and are often structured like you might structure any word document. Webpages usually start with a head, generally containing any information *about* the page itself, rather than information displayed in the actual page, this section includes the title of the webpage to display at the top of the browser window. The information displayed in the actual page is contained in the body, where things like headings, subheadings, and paragraphs break down the information displayed into sections that can be structured.

*Tags:* HTML uses tags to achieve the structure of a webpage. Tags are like labels you can put on a section to provide some information about it. Tags are indicated by characters sitting inside angled brackets, i.e.: <tag>CONTENT</tag>. Most tags come in pairs like the previous example, with one opening tag and one closing tag, which is indicated by starting it with a backslash. The set of tags as well as the content contained with is known as an element, though often times these words are used interchangably. Elements and tags can be elaborated upon using attributes, elaborated upon in it's definition below. 

*View the source code of any website you visit by right clicking and selecting View -> Source or whatever similar option you may see.*

**Definitions:**

Tag
: The "containers" which give some information about the content that lies between an opening and closing tag. Some tags, however, are "empty tags" meaning they only have an opening tag with no closing, such as line break, &lt;br&gt;, or &lt;hr&gt; to add a horizontal line.

Element
: The entire set of both tags, as well as the content contained within them, is referred to as a single element.

Attributes
: Additional information about an element which appears within the opening tag and are made up of a name, an equals sign, and a value assigned to the name. For example, <p lang="en-us">, indicates that the paragraph that follows is written in US English, with lang being the attributes name and "en-us" being the value.

### HTML & CSS Chapter 8: “Extra Markup” (p.176-199)
**Overview:**

*HTML Versions:* The current HTML version is HTML 5. At this point, most users are probably using a web browser that was updated recently enough to support the new features from HTML5, but it can't be expected that all have, so adding support for HTML 4 is still advisable. XHTML is a seperate languages created to bring HTML in line with the ruleset of a different language, XML, which was used to create new markup languages. Each version has it's own DOCTYPE that you use to indicate which you are using in a web page, the standard is <!DOCTYPE HTML> which represents HTML 5.

*Comments:* Placed between <!-- and --> markers, comments are used to add text that isn't displayed on the HTML page but can clarify or add information for yourself in the future or for others who may look at your code and misunderstand some portions. Writing clean and efficient comments is an integral skill to being a proficient programmer.

*Grouping text and elements:* To group multiple elements together in "one block-level box" you use the <div> element. This will allow an entire section of multiple elements such as headings, paragraphs, images, and lists to be combined into one container and given an ID or class for use in CSS styling and for making code better organized and easier to follow. The in-line equivalent to this is the &lt;span&lt; element, which can be used to give a section of text which sits within a larger body of text specific attributes as well, or to group together sets of in-line elements. This element is usually used just for special styling of a certain section of text.
  
*&lt;meta&gt;:* An element that is placed inside the head of a webpage and used to impart certain pieces of information about the webpage to other people or to search engines. A few defined values for the meta attribute are description, keywords, and robots (tells search engines whether or not to add the page to results), these are written as follows: <meta name="description" /n content="Description of content" />. This element also uses the http-equiv and content attributes in pairs in values such as author, pragma (prevents browser from caching the page), and expires (can be used to indicate when a cached version of webpage should expire), these are written as follows: <meta http-equiv="author" /n content="Author Name" />

*Escape Characters:* Some characters are reserved by HTML by default and can't directly be displayed on the webpage, such as angled brackets which are used to indicate tags. If you want to display these characters as the actual character on the webpage, escape characters must be used. Any reserved characters have a code attached to them to display the character, for a left angled bracket &lt; is used, or &gt; for a right angled bracket. There are many of these characters each with their own code, and it is best to always make sure after entering them that they show up correctly, as some fonts do support all of these characters and a special font may need to be specified for them in CSS. Common examples of escape can be found on page 194, but a more complete list can be found online.

**Definitions:**

ID attribute
: Attribute given to an element to assign a unique identification to it, allows for unique styling of that specific element using CSS. i.e. <p id="pullquote">

Class attribute
: Attribute generally given to multiple elements to assign them all to one common group. Also used for styling with CSS, but styles more than one element at a time usually. Multiple classes can be assigned by seperating them with a space i.e. &lt;p class="important admittance"&gt;CONTENT&lt;/p&gt;, which would allow this element to be styled using either the class "important" or "admittance".

Block elements
: Elements that will always start on a new line, such as headings, paragraphs, and lists.

Inline elements
: Elements that will appear on the same line as the neighboring elements, such as images, or font modifications like bolding and italics.

iframe
: Basically a little window embedded in your page, commonly used to show a location on google maps, or to show any other small window within your webpage. A few attributes to keep in mind: src, height, width, scrolling, frameborder, and seamless.

### HTML & CSS Chapter 17: “HTML5 Layout” (pp.428-451)
**Overview:**

*New HTML5 layout elements:* While <div> is good enough for grouping together and organizing related elements, HTML 5 has added a new set of elements to better divide and organize a page. Some common elements from HTML5 are listed and briefly explained below. <div> isn't entirely useless now though, as these new elements are each for specific uses and any groups outside of those specific examples should still be grouped with a <div> element, it is also still used as a wrapper for the entire page. Older browsers that don't use HTML 5 will not recognize these new elements so pg. 442 supplies a piece of code that will tell older versions of HTML to render the new elements as block-level elements, as well as a seperate piece to allow any Internet Explorer verion 8 or below to recognize CSS styling on these new elements as long as they have JavaScript enabled.

**HTML5 Elements:**

Headers and footers:
: &lt;header&gt; and &lt;footer&gt; can be used for an entire webpages header and footer, but also for an individual article or section's header and footer.

Navigation
: &lt;nav&gt; is used for a section that allows the user to navigate around the site.
  
Articles
: &lt;article&gt; is applied to any section that "could stand alone and potentially be syndicated" (pg. 435), such as individual articles on a news page, or one post. Articles can be nested inside one another, such as comments for a blog post.
  
Asides
: &lt;aside&gt; when used within an article should represent information related to the article but that is not entirely necessary, such as a pullquote or a definition of a word. Used outside an article it is for information realted to the entire webpage such as a search bar for the site.

Sections
: &lt;section&gt; is a slightly vague element used to group related content together, each section will usually have it's own heading. It can be used to split a particularly long article into sections, to "contain different sections of the apge, such as latest news, top products, and newsletter signup" (pg. 437), or to group together multiple, related articles. However, &lt;section&gt; should not serve as a wrapper for the whole page.

Heading groups
: &lt;hgroup&gt; is used to contain multiple headings in one group, such as a heading and subsequent subheading, so that both can be treated as a single heading. It has received mixed reaction with some finding little use in it and other finding some use in it.

Figures
: &lt;figure&gt; can be used to contain content referenced by but not integral to the the main article or page, such as images, videos, graphs, diagrams, and code samples. &lt;figcaption&gt; can be used to add a caption for the figure it is contained within.

Linking around block-level elements
: &lt;a&gt; can be used to turn an entire block level element into a link, this is not new to HTML 5 but was not previously seen as a correct use of the &lt;a&gt; tag.

### HTML & CSS Chapter 18: “Process & Design” (pp.452-475)
**Overview:**

*Who's Visiting?:* In making any website it's important that you are designing the site for the target audience as a whole not just for yourself or the site's owner. Consider general questions about your target audience such as an individual's age range, income, and occupation, or a company's size and budget, and anything else that helps to understand your audience better. Fictional people can be made up to represent different areas of your target audience to help understand what different people's needs and wants. It's important to know not only who is visiting, but why. Consider both their key motivations for using the site and what they hope to get out of that use, their ultimate goal on the site. Creating a list of possible reasons people might use your site and applying them to the fictional target audience from before to understand your "customers" better. Once you can picture a user's goal on the site, start to think of what additional infortmation your visitors may find helpful when using your site, the more relevant you appear to a user by answering the needs, the more likely they are to keep using the site. Lastly, determine how frequently your users will visit the site, and how often it needs to be updated, a news website is going to be updated far more than an electrician's website, and some areas may need more frequent updates than others.

*Visual Hierarchy:* Users will rarely read an entire page on the web, they're more likely to skim over the page to find necessary information. Visual Hierarchy refers to the order in which people do that skimming, or in what order a person perceives what they're looking at. It's important to utilize this hierachy effectively, so websites change the appearance of content on a page to facilitate this in the following ways. Size is an obvious one, larger items will be more attention grabbing than smaller ones, which is why headings and key points are usually larger than the rest of the text. Color can also be used to draw attention to a specific message or idea, such as by highly a few words in a paragraph to make them stand out, brighter sections are generally noticed first. Different styles have a similar effect, **bold** and *italic* words are quick to draw people's attention as well. Images are also highly effectively, often being the first thing a person will notice on a page, so they can also be used to facilitate visual hierarchy.

*Organizing:* It's often helpful to group certain elements or components of a webpage together in order to make it easier to comprehend the information. This can be achieved by **proximity**, placing items close together, **closure**, if items are in a complicated arrangement users will attempt to look for some recognizable pattern or form in it, **continuance**, items placed in a line or curve are often seen as more related than those in other arrangements, useful for directing a readers attention in a certain way. **White space**, gaps left between certain items or groups or the lack thereof often implies their relationship to a user, **color**, in the background of a group of items, and **borders** around the items are all common methods to achieve visual grouping. Users will also naturally observe similarities in a webpage, so repetition of things like color, size, orientation, font, etc., can suggest a relationship in importantance or meaning between elements of the webpage as well.

**Definitions:**

Site Maps
: After deciding what information needs to go into your sight generally, a layout of necessary pages or sections and how they will be grouped together. A site map should show how a webpage flows together starting from the home page, or how a user would navigate through it.

Wireframes
: Essentially a mock up of each page of the site's essential information, showing both "the hierarchy of the information and how much space it might require". This is a bare bones sketch of the site, not including any styling choices beyond how the information should be laid out on the page according to the hierarchy of important or key information. Very helpful for making design easier to complete as well as identifying potential functional problems that might be masked by the site's appearance.

## JavaScript:
### Introduction
**Overview:**

*How it's used:* JavaSript can be used for several things within a website: **accessing content**, selecting elements, attributes, or text, **modifying content**, adding or removing those things, **programming rules**, create steps for the browser to follow to access or change content, **reacting to events**, specify that a script should run if a condition is met.

### JS Chapter 1: “The ABC of Programming” (pp.11-52)
**Overview:**

*What is a script and how do I create one?:* A script is a set of steps that you are outlining for a computer to do to achieve some goal. Writing a script involves outlining the steps needed to accomplish the required task, including defining the script's goal, breaking that goal into a series of tasks, visualizing the process in something like a flow chart, and then translating those steps into the necessary code. 

*How do computers fit in with the world around them?:* Computers create "models" of the world using all different kinds of data that we give them. In programming, a physical thing being represented in a code is known as an object. Each object is then ascribed several different things to aid in either creating or acting upon the object. An object's properties tell us certain facts about an object, such as height, weight, color, or any other kind of attribute you could give a real object. Events are the result of some user interaction with an object, programmers need to decide if and when an object reacts this, and then how it will react. Methods are any tasks which are performed using the properties of an object, which can be retrieved and updated. A website's HTML contains many different elements, and each of these creates it's own node, a certain kind of object, and these can be acted upon by JavaScript code.

*How do I write a script for a web page?:* HTML creates the content of the page and gives structure, CSS styles the page by outlining rules for how the HTML content is presented, and JavaScript can change the behavior of the page and add interactivity. JavaScript is best held in it's own file and added to HTML with a &lt;script&gt; tag with a src attribute that gives the storage location of the script, although the code can be written in directly between the script tags in the HTML with no src. JavaScript will not change the HTML of a page, the script is using a model of the web page created by the browser.
