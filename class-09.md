
## Forms

The HTML `<form>` element represents a document section containing interactive controls for submitting information.

Attributes

accept-charset
Space-separated character encodings the server accepts. The browser uses them in the order in which they are listed. The default value means the same encoding as the page.
(In previous versions of HTML, character encodings could also be delimited by commas.)
autocapitalize 
A nonstandard attribute used by iOS Safari that controls how textual form elements should be automatically capitalized. autocapitalize attributes on a form elements override it on <form>. Possible values:
none: No automatic capitalization.
sentences (default): Capitalize the first letter of each sentence.
words: Capitalize the first letter of each word.
characters: Capitalize all characters — that is, uppercase.
autocomplete
Indicates whether input elements can by default have their values automatically completed by the browser. autocomplete attributes on form elements override it on <form>. Possible values:
off: The browser may not automatically complete entries. (Browsers tend to ignore this for suspected login forms; see The autocomplete attribute and login fields.)
on: The browser may automatically complete entries.
name
The name of the form. Deprecated as of HTML 4 (use id instead). It must be unique among the forms in a document and not an empty string as of HTML5.
rel
Creates a hyperlink or annotation depending on the value, see the rel attribute for details.
Attributes for form submission
The following attributes control behavior during form submission.

action
The URL that processes the form submission. This value can be overridden by a formaction attribute on a <button>, <input type="submit">, or <input type="image"> element.
enctype
If the value of the method attribute is post, enctype is the MIME type of the form submission. Possible values:
application/x-www-form-urlencoded: The default value.
multipart/form-data: Use this if the form contains <input> elements with type=file.
text/plain: Introduced by HTML5 for debugging purposes.
This value can be overridden by formenctype attributes on <button>, <input type="submit">, or <input type="image"> elements.

method
The HTTP method to submit the form with. Possible (case insensitive) values:
post: The POST method; form data sent as the request body.
get: The GET method; form data appended to the action URL with a ? separator. Use this method when the form has no side-effects.
dialog: When the form is inside a <dialog>, closes the dialog on submission.
This value is overridden by formmethod attributes on <button>, <input type="submit">, or <input type="image"> elements.

novalidate
This Boolean attribute indicates that the form shouldn't be validated when submitted. If this attribute is not set (and therefore the form is validated), it can be overridden by a formnovalidate attribute on a <button>, <input type="submit">, or <input type="image"> element belonging to the form.
target
Indicates where to display the response after submitting the form. In HTML 4, this is the name/keyword for a frame. In HTML5, it is a name/keyword for a browsing context (for example, tab, window, or iframe). The following keywords have special meanings:
_self (default): Load into the same browsing context as the current one.
_blank: Load into a new unnamed browsing context.
_parent: Load into the parent browsing context of the current one. If no parent, behaves the same as _self.
_top: Load into the top-level browsing context (i.e., the browsing context that is an ancestor of the current one and has no parent). If no parent, behaves the same as _self.
This value can be overridden by a formtarget attribute on a <button>, <input type="submit">, or <input type="image"> element.

***

## LISTS, TABLES AND FORMS

There are several CSS properties that were created to work with specific types of HTML elements, such as lists, tables, and forms.

In this chapter you will learn how to:

Specify the type of bullet point or numbering on lists
Add borders and backgrounds to table cells
Control the appearance of form controls
Together, these properties allow you to take finer control over specific parts of your pages.

![](https://www.oreilly.com/library/view/html-css/9781118206911/images/ch014-Uf001.jpg)

BULLET POINT STYLES
list-style-type
The list-style-type property allows you to control the shape or style of a bullet point (also known as a marker).

It can be used on rules that apply to the <ol>, <ul>, and <li> elements.

![](https://www.oreilly.com/library/view/html-css/9781118206911/images/ch014-Uf002.jpg)

![](https://www.oreilly.com/library/view/html-css/9781118206911/images/ch014-Uf003.jpg)

![](https://www.oreilly.com/library/view/html-css/9781118206911/images/ch014-Uf004.jpg)

UNORDERED LISTS
For an unordered list you can use the following values:

none
• disc
imagecircle
imagesquare


***

## HTML tables

Tables can be a useful way of organising content on a web page, particularly text. A table is defined with the <table> tag. 
Each row in the table is defined with the `<tr>` tag. A table heading is defined with the` <th>` tag. 
 
 Headings are bold and centred by default. Each cell of data in the table is defined with the `<td>` tag.
 Basic table: Set up a table with three headings to your page, by adding the following code to your document under 
 the `“ordered list”` code. This is a real-life example that lists a weekly class schedule. The `<th>` tags will form the columns in this table,
 and the `<td>` tags will form the rows.
  


***
 


# Event reference
DOM Events are fired to notify code of "interesting changes" that may affect code execution.

 These can arise from user interactions such as using a mouse or resizing a window, changes in the 

state of the underlying environment (e.g. low battery or media events from the operating system), and other causes.

Each event is represented by an object that is based on the Event interface, and may have additional custom fields

 and/or functions to provide information about what happened. The documentation for every event has a table (near the top) 

that includes a link to the associated event interface, and other relevant information. A full list of the different event types is given in Event > Interfaces based on Event.

This topic provides an index to the main sorts of events you might be interested in (animation, clipboard, workers etc.) along with the main classes that implement those sorts of events. At the end is a flat list of all documented events.
