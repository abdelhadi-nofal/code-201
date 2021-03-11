## Error Handling & Debugging

JavaScript can be hard to learn and everyone makes
mistakes when writing it. This chapter will help you learn
how to find the errors in your code. It will also teach you how
to write scripts that deal with potential errors gracefully.
When you are writing JavaScript, do not expect to write it perfectly the first time.
Programming is like problem solving: you are given a puzzle and not only do you have to solve
it, but you also need to create the instructions that allow the computer to solve it. too.
When writing a long script, nobody gets everything right in their first attempt. The error
messages that a browser gives look cryptic at first, but they can help you determine what
went wrong in your JavaScript and how to fix it. In this chapter you will learn about:

* THE CONSOLE & DEV TOOLS
Tools built into the browser
that help you hunt for errors.

* COMMON PROBLEMS
Common sources of errors,
and how to solve them.

* HANDLING ERRORS
How code can deal with
potential errors gracefully.

ORDER OF EXECUTION

To find the source of an error, it helps to know how scripts are processed.
The order in which statements are executed can be complex; some tasks
cannot complete until another statement or function has been run:

1. The greeting variable gets its value from the
greetUser() function.
2. greetUser() creates the message by combining
the string 'He 11 o ' with the result of getName ().
3. getName () returns the name to greetUser() .
2. greetUser() now knows the name, and combines
it with the string. It then returns the message to the
statement that ca lled it in step 1.
1. The va lue of the greeting is stored in memory.
4. This greeting variable is written to an alert box.

EXECUTION CONTEXTS

The JavaScript interpreter uses the concept of execution contexts.
There is one global execution context; plus, each function creates a new
new execution context. They correspond to variable scope.


EXECUTION CONTEXT & HOISTING

Each time a script enters a new execution context, there are two phases
of activity:

1: PREPARE
• The new scope is created
• Variables, functions, and arguments are created
• The value of the this keyword is determined

2: EXECUTE
• Now it can assign values to variables
• Reference functions and run their code
• Execute statements

UNDERSTANDING SCOPE

In the interpreter, each execution context has its own variables object.
It holds the variables, functions, and parameters available within it.
Each execution context can also access its parent's variables object.

UNDERSTANDING ERRORS

If a JavaScript statement generates an error, then it throws an exception.
At that point, the interpreter stops and looks for exception-handling code.

ERROR OBJECTS

Error objects can help you find where your mistakes are
and browsers have tools to help you read them.

HOW TO DEAL WITH ERRORS

1: DEBUG THE SCRIPT TO FIX ERRORS
If you come across an error while writing a script
(or when someone reports a bug), you will need to
debug the code, track down the source of the error,
and fix it.
You will find that the developer tools available in
every major modern browser will help you with
this task. In this chapter, you will learn about the
developer tools in Chrome and Firefox. (The tools in
Chrome are identical to those in Opera.)
IE and Safari also have their own tools (but there is
not space to cover them all).

2: HANDLE ERRORS GRACEFULLY
You can handle errors gracefully using try, catch,
throw, and f i na 1 ly statement s.
Sometimes, an error may occur in the script for a
reason beyond your control. For example, you might
request data from a third party, and their server
may not respond. In such cases, it is particularly
important to write error-handling code.
In the latter part of the chapter, you will learn how to
gracefully check whether something will work, and
offer an alternative option if it fails.

A DEBUGGING WORKFLOW

Debugging is about deduction: eliminating potential causes of an error.
Here is a workflow for techniques you will meet over the next 20 pages.
Try to narrow down where the problem might be, then look for clues.

WHERE IS THE PROBLEM?
First, should try to can narrow down the area where
the problem seems to be. In a long script, this is
especially important.
1. Look at the error message, it tells you:
• The relevant script that caused the problem.
• The line number where it became a problem for
the interpreter. (As you will see, the cause of
the error may be earlier in a script; but this is the
point at which the script could not continue.)
• The type of error (although the underlying cause
of the error may be different).
2. Check how far the script is running.
Use tools to write messages to the console to tell
how far your script has executed.
3. Use breakpoints where things are going wrong.
They let you pause execution and inspect the va lues
that are stored in variables.

WHAT EXACTLY IS THE PROBLEM?
Once you think that you might know the rough area
in which your problem is located, you can then try to
find the actual line of code that is causing the error.
1. When you have set breakpoints, you can see if the
variables around them have the values you would
expect them to. If not, look earlier in the script.
2. Break down I break out parts of the code to test
smaller pieces of the functionality.
• Write values of variables into the console.
• Calrfunctions from the console to check if they
are returning what you would expect them to.
• Check if objects exist and have the methods I
properties that you think they do.
3. Check the number of parameters for a function, or
the number of items in an array.

BROWSER DEV TOOLS & JAVASCRIPT CONSOLE

The JavaScript console will tell you when there is a problem with a script,
where to look for the problem, and what kind of issue it seems to be.

These two pages show instructions for opening the
console in all of the main browsers (but the rest of
this chapter will focus on Chrome and Firefox).

Browser manufacturers occasionally change how
to access these tools. If they are not where stated,
search the browser help files for "console."

HOW TO LOOK AT ERRORS IN CHROME

The console will show you when there is an
error in your JavaScript. It also displays the line
where it became a problem for the interpreter.

WRITING FROM THE SCRIPT TO THE CONSOLE

Browsers that have a console have a console object, which has several
methods that your script can use to display data in the console.
The object is documented in the Console API.


LOGGING DATA TO THE CONSOLE

This example shows several uses
of the console . log () method.
1. The first line is used to indicate
the script is running.
2. Next an event handler waits
for the user leaving a text input,
and logs the value that they
entered into that form field.

When the user submits the form,
four values are displayed:
3. That the user clicked submit
4. The value in the width input
5. The value in the height input
6. The value of the area variable
They help check that you are
getting the values you expect.

The console . log() method
can write several values to the
console at the same t ime, each
separated by a comma, as shown
when displaying the height (5).
You should always remove this
kind of error handling code from
your script before you use it on
a live site.

GROUPING MESSAGES

1. If you want to write a set of
related data to the console, you
can use the console. group ()
method to group the messages
together. You can then expand
and contract the results.

2. When you have finished
writing out the results for the
group, to indicate the end of the
group the console .groupEnd ()
method is used.

BREAKPOINTS

You can pause the execution of a script on any
line using breakpoints. Then you can check the
values stored in variables at that point in time.

STEPPING THROUGH CODE

If you set multiple breakpoints, you can step
through them one-by-one to see where values
change and a problem might occur.

When you have set breakpoints,
you will see that the debugger
lets you step through the code
line by line and see the values
or variables as your script
progresses.
When you are doing this, if
the debugger comes across a
function, it will move onto the
next line after the function.
(It does not move to where
the function is defined.) This
behavior is sometimes called
stepping over a function.
If you want to, it is possible
to tell the debugger to step
into a function to see what is
happening inside the function.

1. A pause sign shows until the interpreter comes across a breakpoint.
When the interpreter stops on a breakpoint, a play-style button is then
shown. This lets you tell the interpreter to resume running the code.
2. Go to the next line of code and step through the lines one-by-one
(rather than running them as fast as possible).
3. Step into a function call. The debugger will move to the first line in
that function.
4. Step out of a function that you stepped into. The remainder of the
function will be executed as the debugger moves to its parent function.

THROWING ERRORS

If you know something might cause a problem for your script, you can
generate your own errors before the interpreter creates them.

DEBUGGING TIPS

Here are a selection of practical tips that you
can try to use when debugging your scripts.

* ANOTHER BROWSER
Some problems are browserspecific.
Try the code in another
browser to see which ones are
causing a problem.

* ADD NUMBERS
Write numbers to the console
so you can see which the items
get logged. It shows how far your
code runs before errors stop it.

* STRIP IT BACK
Remove parts of code, and strip
it down to the minimum you
need. You can do this either by
removing the code altogether, or
by just commenting it out using
multi-line comments:
/* Anything between these
characters is a cofllllent */

* EXPLAINING THE CODE
Programmers often report
finding a solution to a problem
while explaining the code to
someone else.

* SEARCH
Stack Overflow is a Q+A site for
programmers.

CODE PLAYGROUNDS
If you want to ask about
problematic code on a forum, in
addition to pasting the code into
a post, you could add it to a code
playground site (such as
JSBin.com, JSFiddle. com, or
Dabbl et. corn) and then post a
link to it from the forum.

VALIDATION TOOLS
There are a number of on line
validation tools that can help you
try to find errors in your code:
JAVASCRIPT
http://www.jslint.com
http://www.jshint .com
JSON
http:// www.jsonlint.com
JQUERY
There is a jQuery debugger
plugin available for Chrome
which can be found in the
Chrome web store.
