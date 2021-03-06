## WHAT IS AN OBJECT?

Objects group together a set of variables and functions to create a model
of a something you would recognize from the real world. In an object,
variables and functions take on new names.

IN AN OBJECT: VARIABLES BECOME KNOWN AS PROPERTIES
If a variable is part of an object, it is called a
**property**. Properties tell us about the object, such as
the name of a hotel or the number of rooms it has.
Each individual hotel might have a different name
and a different number of rooms.

IN AN OBJECT: FUNCTIONS BECOME KNOWN AS METHODS
If a function is part of an object, it is called a **method**.
Methods represent tasks that are associated with
the object. For example, you can check how many
rooms are available by subtracting the number of
booked rooms from the total number of rooms.

## Document Object Model

The Document Object Model (DOM) specifies
how browsers should create a model of an HTML
page and how JavaScript can access and update the
contents of a web page while it is in the browser window.

The DOM is neither part of HTML, nor part of JavaScript; it is a separate set of rules.
It is implemented by all major browser makers, and covers two primary areas:

MAKING A MODEL OF THE
HTML PAGE
When the browser loads a web page, it
creates a model of the page in memory.
The DOM specifies the way in which the
browser should structure this model using
a DOM tree.
The DOM is called an object model
because the model (the DOM tree) is
made of objects.
Each object represents a different part of
the page loaded in the browser window.

ACCESSING AND CHANGING
THE HTML PAGE
The DOM also defines methods and
properties to access and update each
object in this model, which in turn updates
what the user sees in the browser.
You will hear people call the DOM an
Application Programming Interface (API).
User interfaces let humans interact with
programs; APls let programs (and scripts)
talk to each other. The DOM states what
your script can "ask the browser about the
current page, and how to tell the browser
to update what is being shown to the user.

### THE DOM TREE IS A MODEL OF A WEB PAGE

As a browser loads a web page, it creates a model of that page.
The model is called a DOM tree, and it is stored in the browsers' memory.
It consists of four main types of nodes.

#### BODY OF HTML PAGE

`<html>`
    `<body>`
         `<div id="page">`
             `<hl id="header">List</hl>`
             `<h2>Buy groceries</h2>`
              `<ul>`
               `<li id="one" class="hot"><em>fresh</em> figs</li>`
               `<li id="two" class="hot">pine nuts</l i>`
               `<li id="three" class="hot">honey</l i>`
               `<li id="four">balsamic vinegar</l i>`
              `</ul>`
               `<script src="js/l i st. js "></scri pt>`
       `</ div>`
   `</ body>`
`</ html>`

Each node is an object with methods and properties.
Scripts access and update this DOM tree (not the source HTML file).
Any changes made to the DOM tree are reflected in the browser.

### DOM TREE

![](https://i.imgur.com/wgwdNL6.png)

* ATTRIBUTE NODES
The opening tags of HTML elements can carry
attributes and these are represented by attribute
nodes in the DOM tree.
Attribute nodes are not children of the element that
carries them; they are part of that element. Once
you access an element, there are specific JavaScript
methods and properties to read or change that
element's attributes. For example, it is common to
change the values of cl ass attributes to trigger new
CSS rules that affect their presentation.

* TEXT NODES
Once you have accessed an element node, you
can then reach the text within that element. This is
stored in its own text node.
Text nodes cannot have children. If an element
contains text and another child element, the child
element is not a child of the text node but rather
a child of the containing element. (See the `<em>`
element on the first `<li>` item.) This illustrates how
the text node is always a new branch of the DOM
tree, and no further branches come off of it.


WORKING WITH THE DOM TREE

Accessing and updating the DOM tree involves two steps:
1: Locate the node that represents the element you want to work with.
2: Use its text content, child elements, and attributes.

ACCESSING ELEMENTS
DOM queries may return one element, or they may return a Nodelist,
which is a collection of nodes.
Sometimes you will just want to access one
individual element (or a fragment of the page that
is stored within that one element). Other times you
may want to select a group of element s, for example,
every <hl> element in the page or every <1i>
element within a particular list.

SELECTING ELEMENTS USING ID ATTRIBUTES

getElementByid () al lows you
to select a single element node
by specifying the value of its
id attribute.
This method has one parameter:
the value of the id attribute on
the element you want to select.
This value is placed inside quote
marks because it is a string. The
quotes can be single or double
quotes, but they must match.
In the example on the left, the
first line of JavaScript code finds
the element whose id attribute
has a value of one, and stores
a reference to that node in a
variable called e1.

NODELISTS: DOM QUERIES THAT RETURN MORE THAN ONE ELEMENT
When a DOM method can return more than one element, it returns a
Nodelist (even if it only finds one matching element).
A Nodelist is a collection of element nodes. Each
node is given an index number (a number that starts
at zero, just like an array).
The order in which the element nodes are stored in a
Node List is the same order that they appeared in the
HTML page.
When a DOM query returns a Nodelist, you may
want to:
• Select one element from the NodeList.
• Loop through each item in the Nodelist and
perform the same statements on each of the
element nodes.


SELECTING AN ELEMENT FROM A NODELIST

There are two ways to select an element from a Nodelist:
The item() method and array syntax.
Both require the index number of the element you want.
THE ;tern{) METHOD
Nodelists have a method
called item() which will return
an individual node from the
Node list.
You specify the index number
of the element you want as a
parameter of the method (inside
the parentheses).

`var elements = document.getElementsByClassName('hot')`
`if (elements.length>= 1) {`
`var firstltem = elements.item(O);`
`}`


SELECTING ELEMENTS USING CLASS ATTRIBUTES

The get ElementsByCl ass Name()
method allows you to select
elements whose c 1 ass attribute
contains a specific value.
The method has one parameter:
the class name which is given
in quotes within the parentheses
after the method name.
Because several elements can
have the same value for their
cl ass attribute, this method
always returns a Nodelist.

SELECTING ELEMENTS BY TAG NAME

The get El ementsByTagName ()
method allows you to select
elements using their tag name.
The element name is specified
as a parameter, so it is placed
inside the parentheses and is
contained by quote marks.
Note that you do not include the
angled brackets that surround
the tag name in the HTML (just
the letters inside the brackets).

SELECTING ELEMENTS USING CSS SELECTORS

querySe1ector() returns
the first element node that
matches the CSS-style selector.
querySe1ectorA11 () returns a
Nodelist of all of the matches.
Both methods take a CSS
selector as their only parameter.
The CSS selector syntax offers
more flexibility and accuracy
when selecting an element than
just specifying a class name
or a tag name, and should also
be familiar to front-end web
developers who are used to
targeting elements using CSS.

LOOPING THROUGH A NODELIST

If you want to apply the same
code to numerous elements,
looping through a Nodelist is a
powerful technique.
It involves finding out how many
items are in the Nodelist, and
then setting a counter to loop
through them, one-by-one.
Each time the loop runs, the
script checks that the counter
is less than the total number of
items in the Nodelist.

`var hotltems = document .querySelectorAll (' li . hot') ; II Store Nodelist in array`
`if (hot ltems.length > O) { II If it contains i t ems`
`for (var i=O; i<hotl tems.length; i++) { II Loop through each item`
`hotltems[i ] .className = 'cool'; II Change value of class at tribute`
`}`


TRAVERSING THE DOM

When you have an element node, you can select
another element in relation to it using these five
properties. This is known as traversing the DOM.

* parentNode
This property finds the element
node for the containing (or
parent) element in the HTML.
(1) If you started with the
first <l i >element, then its
parent node would be the one
representing the <ul >element.

* previousSibling nextSibling
These properties find the
previous or next sibling of a node
if there are siblings.
If you started with the first <1i >
element, it would not have a
previous sibling. However, its next
sibling (2) would be the node
representing the second <li >.

firstChild lastChild
These properties find the first or
last child of the current element.
If you started with the <u1>
element, the first child would be
the node representing the first
<l i> element, and (3) the last
child would be the last <1i>.


WHITESPACE NODES
Traversing the DOM can be difficult because
some browsers add a text node whenever they
come across whitespace between elements.

PREVIOUS & NEXT SIBLING
You have just seen that
these properties can return
inconsistent results in different
browsers. However, it is safe
to use them when there is no
whitespace between elements.
For this example, all spaces
between the HTML elements
have been removed. In order to
demonstrate these properties,
the second list item is selected
using getElementByld ().

From this element node, the
previ ousSi b 1 i ng property will
return the first <1 i> element,
and the next Sib 1 i ng property
will return the third <1 i>
element.

`<ul><li id="one" class="hot"><em>fresh<l em> figs<l li><li id="two"`
`class="hot">pine nuts<l li><li id="three" class="hot">honey<l li><li`
`id="four">balsamic vinegar<lli><lul>`

FlRST & LAST CHILD
These properties also return
inconsistent resu lts if there is
whitespace between elements.
In this example, a slightly
different solution is used in the
HTML - the closing tags are put next to the opening tags of
the next element, making it
a little more readable. The
example starts by using the
getElementsByTagName()
method to select the <ul>
element from the page. From this
element node, the fi rstChi 1 d
property will return the first <1i>
element, and the 1 as tChi 1 d
property will return the last <li>
element.

`<ul>`
`><li id="one" class="hot"><em>fresh</em> figs </li`
`><li id="two" class="hot">pine nuts</li`
`><li id="three" cl ass="hot">honey<lli`
`><li id="four">balsamic vinegar</li>`
`</ul>`

HOW TO GET/UPDATE ELEMENT CONTENT

So far this chapter has focused on finding elements in the DOM tree.
The rest of this chapter shows how to access/update element content.
Your choice of techniques depends upon what the element contains.

ACCESS & UPDATE A TEXT NODE WITH NODEVALUE
When you select a text node, you can retrieve or amend the content of it
using the node Va1ue property.

ACCESSING & CHANGING A TEXT NODE
To work with text in an element, first the element node is
accessed and then its text node.The text node has a property
called node Value which returns
the text in that text node. You can also use the node Va 1 ue
property to update the content
of a text node.

ACCESS & UPDATE TEXT WITH TEXTCONTENT (& INN ERTEXT)

The textContent 
property allows you to
collect or update just the text that is in the
containing element (and its children).
textContent
To collect the text from the
<l i> elements in our example
(and ignore any markup inside
the element) you can use the
textContent property on the
containing <l i > element. In this
case it would return the value:
fresh figs.
You can also use this property
to update the content of the
element; it replaces the entire
content of it (including any
markup).

innerText
You may also come across a property called i nner Text, but you should generally avoid it for three key reasons:
* SUPPORT
Although most browser manufacturers adopted the
property, Firefox does not because innerText is not part of
any standard.

* OBEYS CSS
It will not show any content
that has been hidden by CSS.
For example, if there were a CSS
rule that hid the <em> elements,
the i nnerText property would
return only the word figs.

* PERFORMANCE
Because the i nnerText property
takes into account layout rules
that specify whether the element
is visible or not, it can be slower
to retrieve the content than the
textContent property.

ACCESSING TEXT ONLY
In order to demonstrate the
difference between textContent
and i nnerText, this example
features a CSS rule to hide the
contents of the <em> element.
The script starts off by getting
the content of the first list item
using both the textContent
property and i nnerText. It then
writes the values after the list.
Finally, the value of the first
list item is then updated to say
sourdough bread. This is done
using the textContent property.

ACCESS & UPDATE TEXT & MARKUP WITH INNERHTML

Using the i nnerHTML property, you can access
and amend the contents of an element,
including any child elements.

UPDATE TEXT & MARKUP

This example starts by storing
the first list item in a variable
called firstltem.
It then retrieves the content of
t his list item and stores it in a
variable called itemContent.
Finally, the content of the list
item is placed inside a link. Note
how the quotes are escaped.

ADDING ELEMENTS USING DOM MANIPULATION

DOM manipulation offers another technique
to add new content to a page (rather than
innerHTML). It involves three steps:

1. 
CREATE THE ELEMENT
createEl ement ()
You start by creating a new
element node using the
createElement() method.
This element node is stored
in a variable.
When the element node is
created, it is not yet part of the
DOM tree. It is not added to
the DOM tree until step 3.

2. 
GIVE IT CONTENT
createTextNode()
createTextNode() creates a new text node. Again, the node is stored in a variable. It can be
added to the element node using the appendChild () method.
This provides the content for the element, although you can skip this step if you want to attach an
empty element to the DOM tree.

3. 
ADD IT TO THE DOM
appendChild()
Now that you have your element (optionally with some content in a text node), you can add
it to the DOM tree using the appendChi 1 d () method. The appendChi1d () method allows you to specify which
element you want this node added to, as a child of it.

ADDING AN ELEMENT TO THE DOM TREE

createElement () creates an
element that can be added to the
DOM tree, in this case an empty
<l i >element for the list.
This new element is stored
inside a variable called newEl
until it is attached to the DOM
tree later on.
createTextNode() allows you to
create a new text node to attach
to an element. It is stored in a
variable called newText.


REMOVING ELEMENTS VIA DOM MANIPULATION

DOM manipulation can be used to remove
elements from the DOM tree.

REMOVING AN ELEMENT FROM THE DOM TREE
This example uses the
removeChi1d () method to
remove the fourth item from the
list (along with its contents).
The first variable, removeEl,
stores the actual element you
want to remove from the page
(the fourth list item).
The second variable,
cont a i nerEl, stores the <u 1 >
element that contains the
element you want to remove.

COMPARING TECHNIQUES: UPDATING HTML CONTENT

So far, you have seen three techniques for adding HTML to a web page.
It's time to compare when you should use each one.
In any programming language, there are often
several ways to achieve the same task. In fact, if you
asked ten programmers to write the same script, you
may well find ten different approaches.
Some programmers can be rather opinionated and
believe that their way is always the "right" way to do
things - when there are often several right ways. If
you understand why people prefer some approaches
over others, then you are in a strong position to
decide whether it meets the needs of your project.

CROSS-SITE SCRIPTING (XSS) ATTACKS

If you add HTML to a page using i nnerHTML (or several jQuery methods),
you need to be aware of Cross-Site Scripting Attacks or XSS; otherwise,
an attacker could gain access to your users' accounts.


DEFENDING AGAINST CROSS-SITE SCRIPTING

VALIDATE INPUT GOING TO THE SERVER
1. Only let visitors input the kind
of characters they need to when
supplying information. This is
known as validation. Do not
allow untrusted users to submit
HTML markup or JavaScript.

2. Double-check validation on
the server before displaying user
content/storing it in a database.
This is important because users
could bypass validation in the
browser by turning JavaScript off.

3. The database may safely
contain markup and script
from trusted sources (e.g., your
content management system).
This is because it does not try to
process the code; it just stores it.

XSS: VALIDATION & TEMPLATES

Make sure that your users can only input characters they need to use
and limit where this content will be shown on the page.

XSS: ESCAPING & CONTROLLING MARKUP

Any content generated by users that contain characters that are used
in code should be escaped on the server. You must control any markup
added to the page.

CHECK FOR AN ATTRIBUTE AND GET ITS VALUES

Before you work with an
attribute, it is good practice to
check whether it exists. This will
save resources if the attribute
cannot be found.
The hasAttribute() method
of any element node lets you
check if an attribute exists. The
attribute name is given as an
argument in the parentheses.
Using hasAttribute() in an if
statement like this means that
the code inside the curly braces
will run only if the attribute
exists on the given element.

CREATING ATTRIBUTES & CHANGING THEIR VALUES
The cl assName property allows
you to change the value of the
cl ass attribute. If the attribute
does not exist, it will be created
and given the specified value.
You have seen this property
used throughout the chapter
to update the status of the
list items. Below, you can see
another way to achieve the task.
The setAttri bute() method
allows you to update the va lue
of any attribute. It takes two
parameters: the attribute name,
and the value for the attribute.

REMOVING ATTRIBUTES
To remove an attribute from an
element, first select the element,
then call removeAttribute () .
It has one parameter: the name
of the attribute to remove.
Trying to remove an attribute
that does not exist will not cause
an error, but it is good practice
to check for its existence before
attempting to remove it.

In this example, the
get ElementByld () method is
used to retrieve the first item
from this list, which has an id
attribute with a value of one.

EXAMINING THE DOM IN CHROME
Modern browsers come with tools that help
you inspect the page loaded in the browser
and understand the structure of the DOM tree.

EXAMINING THE DOM IN FIREFOX
Firefox has similar built-in tools, but you can
also download a DOM inspector tool that
shows the text nodes.


***

## Understanding The Problem Domain Is The Hardest Part Of Programming 

What is the hardest thing about writing code?

There are many common answers to this question:

Learning a new technology
Naming things
Testing your code
Debugging
Fixing bugs
Making software maintainable
The list goes on and on.

But as I reflect back on my programming career, and I’ve conversed with many new programmers that are learning the craft, I’ve found the single hardest thing about programming is learning the problem domain.

A familiar problem
In a good portion of my Pluralsight courses I show the viewer how to build the “Protein Tracker” application.

I am often asked why I keep demonstrating how to build the same simple application over and over again in each of my courses.

The answer is “familiarity.”

When I first started using the Protein Tracker example in my Android course, I was just looking for a simple example of an application that could be easily understood and implemented.

The idea behind the Protein Tracker application is that it allows a user to set a goal for the amount of protein to consume in a day.  The user can add protein amounts which are added to a total protein count that is tracked for that user.

![](http://i0.wp.com/simpleprogrammer.com/wp-content/uploads/2013/07/Protein_Tracker_2013-07-03_16-44-41_thumb.png?resize=506%2C219)


Very simple functionality, easily explainable, but most importantly, easily understood.

What I found with this simple application was that because it was so easy to understand, the focus was taken off of the problem domain and put instead on the technology.

Not only this, but as I reused this same exact application for teaching a variety of different technologies, it served as a reference problem domain that didn’t have to be re-learned, and provided a way to compare and contrast different technologies—I was getting this teaching mechanism for free if a viewer had already watched one of my other Pluralsight courses.

By creating a familiar problem domain, I found that both the tasks of me teaching a new technology and the viewer learning that technology were much easier, because it is very difficult to learn more than one thing at once.

So what am I trying to say here?

Simply that by taking away the problem domain, or making it so trivial that it is easily understood, I am able to make both teaching and learning easier.

Why problem domains are hard
Have you ever tried to put together a jigsaw puzzle that didn’t have any picture on it?  How about one like this one, that has a very similar pattern repeated on it and is double-sided?

The reason why puzzles like this one are so hard, is because you can’t really see what you are trying to build very clearly.  Normally when you put together a jigsaw puzzle you follow steps that might look something like this:

Figure out what the major components of the picture are
Sort the pieces by color or component
Put together all the border pieces
Put together each component of the picture from the piles you created
This all breaks down when you don’t have a picture with clear components that you can identify.

The same thing happens when writing code.  Writing code is a lot like putting together a jigsaw puzzle.  We put together code with the purpose of building components that we have taken out of the “bigger picture” of the problem domain.

The big issue is that many problem domains are like a puzzle with a blurry picture or no picture at all.

The real world is a messy place.  Many of the problem domains we face as programmers are difficult to understand and look completely different depending on your viewpoint.

As programmers, we also are often not given complete information about the problem domain, so we don’t even have the information we need to understand it.

Just try and read the famous Domain Driven Design book and you’ll quickly see how complicated and difficult problem domains can be.  (Great book by the way, although you may have to read it twice or three times—I certainly did.)

Programming is easy if you understand the problem domain

A long time ago, I worked for Hewlett Packard writing software for multi-function printers.

Most of the work at the time was basic waterfall development.  There wasn’t much Agile happening there—at least at the time I was there.waterfall can define problem domains

There was however something really interesting about the waterfall approach and the extreme amount of specification that was done before anything was built—it was very easy to write the code for a feature.

I remember writing a tab control for the user interface of a printer and having the complete pixel perfect specs handed to me before I began to write any code.  I was also given all the possible use cases and told exactly how it should function and what it should do under just about every circumstance.

Guess how easy it was to write the code to produce this tab control?  Super easy.

What can you do about it?
If understanding the problem domain is the hardest part of programming and you want to make programming easier, you can do one of two things:

Make the problem domain easier
Get better at understanding the problem domain
You can often make the problem domain easier by cutting out cases and narrowing your focus to a particular part of the problem.

What I mean by this is that it is often beneficial to take a part of the problem and fully understand that part before expanding the problem domain.

Games are really good at this.  Look at most games today and you’ll find that you start with a very small problem domain.  The first level is usually a tutorial that has a basic set of things you can do so that you don’t get overwhelmed.  But, as you advance through the levels, you usually find they get harder and introduce new concepts that build gradually on what you know, until you understand a pretty large problem domain.  (Starcraft is really good at this.)

The other choice is to become better at understanding problem domains.  As developers, we tend to think that sitting down and talking to customers or business people who know about the problem domain is a waste of time. It is easy to fall into the trap of thinking you understand enough of the problem to get started coding it.  Best to resist the temptation to “not waste anymore time talking” and make sure you understand a problem inside and out before you try and solve it with code.  It is much more expensive and time consuming to do things over than it is to do them right the first time.  I learn this lesson the hard way time and time again.

Quick update on my new product
I’m still not ready to unveil exactly what I am building, but I do have an active mailing list where you can sign up to find out when I release the product I’m working on to help developers get better career opportunities and market themselves.

So many developers don’t realize how much of an impact marketing themselves and branding can have on their opportunities.  I’m hoping to help developers learn not only how valuable marketing and branding is, but how to do it most effectively.

If you are interested, please sign up. (I won’t spam you.)
