## HTML TEXT

When creating a web page, you add tags (known as markup) to the contents of the
page. These tags provide extra meaning and allow browsers to show users the appropriate structure for the page.
 In this chapter we focus on how to add markup to the text that appears on your pages. You will learn about:

● Structural markup: the elements that you can use to describe both headings and paragraphs.

● Semantic markup: which provides extra information; such as where emphasis is placed in a sentence, that something
 you have written is a quotation (and who said it), the meaning of acronyms, and so on.


### Headings

`<h1>`
`<h2>`
`<h3>`
`<h4>`
`<h5>`
`<h6>`

`<h1>This is a Main Heading</h1>`
`<h2>This is a Level 2 Heading</h2>`
`<h3>This is a Level 3 Heading</h3>`
`<h4>This is a Level 4 Heading</h4>`
`<h5>This is a Level 5 Heading</h5>`
`<h6>This is a Level 6 Heading</h6>`

### Paragraph 
`<p>`

To create a paragraph, surround the words that make up the paragraph with an opening `<p>`
tag and closing `</p>` tag.

### Bold & Italic
`<b><i>`

### Superscript & Subscript
`<sup> <sub>`

### Line Breaks & Horizontal Rules
`<br /> <hr />`

### Visual Editors & Their Code views

Content management systems and HTML editors such as Dreamweaver
usually have two views of the page you are creating: a visual editor and a
code view.

Visual editors often resemble word processors. Although
each editor will differ slightly, there are some features that are common to most editors
that allow you to control the presentation of text.

### Semantic Markup

There are some text elements that are not intended to affect the
structure of your web pages, but they do add extra information to the
pages — they are known as semantic markup.

### Strong & Emphasis

`<strong> <em>`

### Quotations

`<blockquote> <q>`

### Abbreviations & Acronyms
`<abbr>`

### Citations & Definitions
`<cite> <dfn>`

### Author Details

`<address>`

### Changes to Content

`<ins>`
`<del>`
`<s>`

### EXAMPLE :

`<html>`
`<head>`
`<title>Text</title>`
`</head>`
`<body>`
`<h1>The Story in the Book</h1>`
`<h2>Chapter 1</h2>`
`<p>Molly had been staring out of her window for about`
`an hour now. On her desk, lying between the copies`
`of <i>Nature</i>, <i>New Scientist</i>, and all`
`the other scientific journals her work had`
`appeared in, was a well thumbed copy of <cite>On`
`The Road</cite>. It had been Molly's favorite book`
`since college, and the longer she spent in these`
`four walls the more she felt she needed to be`
`free.</p>`
`<p>She had spent the last ten years in this room,`
`sitting under a poster with an Oscar Wilde quote`
`proclaiming that <q>Work is the refuge of`
`people who have nothing better to do</q>. Although`
`many considered her pioneering work, unraveling`
`the secrets of the llama <abbr`
`title="Deoxyribonucleic acid">DNA</abbr>, to be an`
`outstanding achievement, Molly <em>did</em> think`
`she had something better to do.</p>`
`</body>`
`</html>`


***


## Introducing CSS

### CSS Associates Style rules with HTML elements
CSS works by associating rules with HTML elements. These rules govern
how the content of specified elements should be displayed. A CSS rule
contains two parts: a selector and a declaration.

### CSS Properties Affect How Elements Are Displayed

CSS declarations sit inside curly brackets and each is made up of two
parts: a property and a value, separated by a colon. You can specify
several properties in one declaration, each separated by a semi-colon.

### Using External CSS

`<link>`
The <link> element can be used
in an HTML document to tell the
browser where to find the CSS
file used to style the page. It is an
empty element (meaning it does
not need a closing tag), and it
lives inside the <head> element.
It should use three attributes:

`href`
`type`
`rel`

### Using Internal CSS

`<style>`

You can also include CSS rules within an HTML page by placing
them inside a `<style>` element, which usually sits inside the
`<head>` element of the page. The `<style>` element should use
the type attribute to indicate that the styles are specified in
CSS. The value should be text/ css.

### CSS Selectors

There are many different types of CSS selector that allow you to
target rules to specific elements in an HTML document.

### Why use External Style Sheets?

When building a website there are several advantages to placing your
CSS rules in a separate style sheet.

All of your web pages can share the same style sheet. This is
achieved by using the `<link>` element on each HTML page of
your site to link to the same CSS document. This means that the
same code does not need to be repeated in every page (which
results in less code and smaller HTML pages).

### Different versions of CSS & Browser Quirks

CSS1 was released in 1996 and CSS2 followed two years later. Work on
CSS3 has been ongoing but the major browsers have already started to
implement it.

***

## Basic JavaScript Instructions

### STATEMENTS

script is a series of instructions that a computer can follow one-by-one.
Each individual instruction or step is known as a statement.
Statements should end with a semicolon.

### COMMENTS

You should write comments to explain what your code does.
They help make your code easier to read and understand.
This can help you and others who read your code.

### WHAT IS A VARIABLE?

A script will have to temporarily store the bits of information it
needs to do its job. It can store this data in variables.

### DATA TYPES

NUMERIC DATA TYPE 0.75
STRING DATA TYPE 'H.1'
BOOLEAN DATA TYPE true,false

### RULES FOR NAMING VARIABLES

1
The name must begin with
a letter, dollar sign ($),or an
underscore (_). It must not start
with a number.

2
The name can contain letters,
numbers, dollar sign ($), or an
underscore (_). Note that you
must not use a dash(-) or a
period (.) in a variable name.

3
You cannot use keywords or
reserved words. Keywords
are special words that tell the
interpreter to do something. For
example, var is a keyword used
to declare a variable. Reserved
words are ones that may be used
in a future version of JavaScript.
ONLINE EXTRA
View a full list of keywords and
reserved words in JavaScript.

4
All variables are case sensitive,
so score and Score would be
different variable names, but
it is bad practice to create two
variables that have the same
name using different cases.

5
Use a name that describes the
kind of information that the
variable stores. For example,
fi rstName might be used to
store a person's first name,
l astNarne for their last name,
and age for their age.

6
If your variable name is made
up of more than one word, use a
capital letter for the first letter of
every word after the first word.
For example, f i rstName rather
than fi rstnarne (this is referred
to as camel case). You can also
use an underscore between each
word (you cannot use a dash).

### ARRAYS

An array is a special type of variable. It doesn't
just store one value; it stores a list of values.

### EXPRESSIONS

An expression evaluates into (results in) a single value. Broadly speaking
there are two types of expressions.

### OPERATORS

Expressions rely on things called operators; they allow programmers to
create a single value from one or more values.

### EXAMPLE :

`<!DOCTYPE html>`
`<html>`
`<head>`
`1111., .• ,`
`<title>JavaScript &amp; jQuery - Chapter 2: Basic JavaScript Instructions -`
`Example</ title>`
`<link rel="stylesheet" href="css/c02.css" />`
`</head>`
`<body>`
`<hl>Elderflower</hl>`
`<div id="content">`
`<div id="greeting" class="message">Hello! </div>`
`<table>`
`<tr>`
`<td>Custom sign: </ td>`
`<td id="userSign"></ td>`
`</ tr>`
`<tr>`
`<td>Total tiles: </td>`
`<td id="ti l es "></td>`
`</tr>`
`<tr>`
`<td>Subtotal: </td>`
`<td id="subTotal">$</ td>`
`</ tr>`
`<tr>`
`<td>Shipping: </ td>`
`<td id="shipping">$</td>`
`</tr>`
`<tr>`
`<td>Grand total: </td>`
`<td id="grandTotal ">S</td>`
`</tr>`
`</ table>`
`<a href="D" class="action">Pay Now</ a>`
`</div>`
`<script src="js/ example.js"></ script>`
`</body>`
`</html>`

*** 

## Decisions and Loops

Decision Making Statements
Decision Making in programming is similar to decision making in real life.
A programming language uses control statements to control the flow of execution of the program based on certain conditions.
JavaScript’s conditional statements are:
1) if
2) if-else
3) if…else…if
4) switch
1) if statement
if statement is the most simple decision making statement.
It is used to decide whether a certain statement or block of statements will be executed or not.
If a certain condition is true then a block of statement is executed otherwise not.
Syntax
`if ( condition ) `
`{`
   `// block of code to be executed`
`}`

2) if…else statement
The if-else statement has two parts if block and else block.
If the condition is true then if block (true block) will get executed and if the condition is false then else block (false block) will get executed.
Syntax

`if ( condition )  `
`{`
    `// block of code to be executed when condition is true`
`} `
`else `
`{`
    `// block of code to be executed when condition is false`
`}`

3) if…else...if statement
The if…else…if statement statement is an advanced form of if…else that allows JavaScript to make a correct decision out of several conditions.
All the if conditions will be checked one by one. If any condition is true out of given then that block will get executed and other blocks are skipped.
Syntax

`if ( condition 1 )  `
`{`
    `// block of code to be executed when condition 1 is true`
`} `
`else if ( condition 2 )  `
`{`
    `// block of code to be executed when condition 2 is true`
`} `
`else if ( condition 3 )  `
`{`
    `// block of code to be executed when condition 2 is true`
`}`
`else`
`{`
   `// block of code to be executed if no condition matches`
`}`

4) switch statement
The objective of a switch statement is to give an expression to evaluate and several different statements to execute based on the value of the expression.
The interpreter checks each case against the value of the expression until a match is found. If nothing matches, a default condition will be used.
Syntax

`switch (expression) `
`{`
   `case c1: statement(s)`
            `break;`
   
   `case c2: statement(s)`
            `break;`
   `...`
   
   `case cn: statement(s)`
            `break;`
   
   `default: statement(s)`
`}`

Looping Statements
Looping in programming languages facilitates the execution of a set of instructions/functions repeatedly while some condition evaluates to true.
For example, suppose we want to print “Hello World” 10 times this is possible with the help of loops.
There are mainly two types of loops:
1) Entry Controlled loops: In this type of loops the test condition is tested before entering the loop body. For Loop and While Loop are entry controlled loops.
2) Exit Controlled Loops: In this type of loops the test condition is tested or evaluated at the end of loop body. Therefore, the loop body will execute atleast once, irrespective of whether the test condition is true or false. do-while loop is exit controlled loop.
Following are the types of loops in JavaScript:
1) while loop
2) do-while loop
3) for loop
4) for…in loop
1) while loop
A while loop is a entry-controlled loop that allows code to be executed repeatedly if the condition is true.
When the condition becomes false, the loop terminates which marks the end of its life cycle.
The while loop executes ZERO or MORE times.
Syntax

`while (condition)`
`{`
   `// Statements to be executed`
`}`

2) do-while loop
A do-while loop is a exit-controlled loop that allows code to be executed first and after that checks for condition and depending on that it executed repeatedly.
When the condition becomes false, the loop terminates which marks the end of its life cycle.
The do-while loop executes ONE or MORE times.
Syntax

`do`
`{`
    `// Statements to be executed`
`}  while (condition);`

3) for loop
A for loop is a entry-controlled loop that allows code to be executed repeatedly.
It provides a concise way of writing the loop structure.
Unlike a while loop, a for statement consumes the initialization, condition and increment/decrement in one line thereby providing a shorter, easy to debug structure of looping.
The for loop executes ZERO or MORE times
Syntax

`for (initialization; condition; increment/decrement)`
`{`
    `// Statements to be executed`
`}`

4) for…in loop
JavaScript also includes another version of for loop also known as the for..in loops.
The for..in loop provides a simpler way to iterate through the properties of an object.
This loop is seen to be very useful while working with objects.
In each iteration, one of the properties of Object is assigned to the variable named variableName and this loop continues until all of the properties of the Object are processed.
Syntax

`for (variableName in Object)`
`{`
    `// Statements to be executed`
`}`

### SAMPLE PROGRAMS
Develop a JS program to display numbers from 1 to 10.

`<html>`
    `<head>`
        `<title>Display Numbers from 1 to 10</title>`
    `</head>`
    `<body>`
        `<h3>Numbers from 1 to 10 are</h3>`
        `<script type="text/javascript">`
            `var a = 1; `
  
            `while (a <= 10) `
            `{ `
                `document.write(a + "<br />"); `
                `a++; `
            `}`
        `</script>`
    `</body>`
`</html>`






