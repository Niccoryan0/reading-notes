# 401-02 Readings

## Unit Testing Best Practices *Not in Xunit, but concepts are still true
[Link](https://stackify.com/unit-testing-basics-best-practices/)\
A few things unit tests DON'T do:
- Deal w/ environment/external systems in the code base
- Require "proper setup" to run
- Throw thousands of requests for a service (smoke testing)
- Generate random data to test to run the application with
- Exercise multiple components of the systema and how it acts. "If you have a console application and you pipe input to it from the command line and test for output, you’re executing an end-to-end system test — not a unit test."\
Unit tests "isolate and exercise specific *units* of your code". In C# that means testing something specific about a method, which would be considered a *unit*.\
A test can be as simple as writing a method that returns x+y, and then a unit test which says does my method equal 11 when passed 5 and 6 as arguments. This is tedious to do for many methods, writing an individual test, and even making a test method and calling it when necessary becomes too laborious. Fortunately we now have frameworks for unit testing that make the process and execution quicker and more fruitful, and Visual Studio has built in templates for unit testing. See article for example of basic test.\
**Basic Practices of Unit Testing: **
- Arrange, Act, Assert: Similar to the scientific method, we hypothesize that 4 and 3 will be 7 when passed into our addition method, we *arrange* everything, in this case just instantiate the calculator object but it can be more complex, *act* or invoke our adde method and capture the result, and *assert* whether the test passed or not, or whether the hypothesis was correct.
- One Assert Per Test Method: Not universally believed but the author makes the argument that east test should be a self contained single hypothesis and test essentially.
- Avoid Test Interdependence: Make sure tests don't rely on other tests to be run, this can be overlooked by accident if testing is always done in the same order.
- Keep It Short, Sweet and Visible: "Resist the impulse to abstract test setup (the “arrange”) to other classes, and especially resist the impulse to abstract it into a base class."
- Recognize Test Setup Pain as a Smell: Not important early on, but in real world application: "If you find that the “arrange” part of your unit test becomes cumbersome, stop what you’re doing.  One of the most undercover powerful things about unit tests is that they provide excellent feedback on the design of your code — specifically its modularity.  If you find yourself laboring heavily to get a class and method setup so that you can test it, you have a design problem.

When you create setup heavy tests, you create brittle tests.  Tests carry a maintenance weight, just like production code.  You thus want to avoid unwieldy tests like the plague — they’ll break and make you and everyone else hate them.  So instead of going nuts on the setup, take a critical look at your design."
- Add Them to the Build: Seems self explanatory, if a test fails the build fails.

## XUnit Documentation
[Link](https://xunit.github.io/#documentation)\
Bookmarked, not sure if notes are required for this part? I glanced through the documentation home page.

## Art of Readme
[Link](https://github.com/noffle/art-of-readme)\
Interesting tidbit: "The pattern of README appearing in all-caps is a consistent facet throughout history. In addition to the visual strikingness of using all-caps, UNIX systems would sort capitals before lower case letters, conveniently putting the README before the rest of the directory's content."\
READMEs should:
- Tell a user what the project is
- How it looks in action
- How to use it
- Any other relevant details\
Key elements of a README include: Name, One-Liner, Usage, API (details module's objects and functions, signatures, return types, callbacks and events in detail.), Installation, and License. The README should be laid out in a predictable format with key elements present to facilitate cognitive funnelling,\"...can be imagined as a funnel held upright, where the widest end contains the broadest more pertinent details, and moving deeper down into the funnel presents more specific details that are pertinent for only a reader who is interested enough in your work to have reached that deeply in the document. Finally, the bottom can be reserved for details only for those intrigued by the deeper context of the work (background, credits, biblio, etc.)."\
In general just ensure that a README is easily digestible to the target audience, contains all the relevant information, links, background, etc. that they might need, and make sure it's just generally robust.


## ReadMe Best Practices
[Link](https://github.com/jehna/readme-best-practices)\
Good template for making READMEs, can be downloaded and changed to fit your project.\
*Taken from README:*\
This project makes it easy to:
- Bootstrap your open source project properly
- Make sure everyone gets what you're trying to achieve with your project
- Follow simple instructions for a perfect README.md