## Images in HTML

n the beginning, the Web was just text, and it was really quite boring. Fortunately,
 it wasn't too long before the ability to embed images (and other more interesting types of content)
 inside web pages was added. There are other types of multimedia to consider,
 but it is logical to start with the humble `<img>` element, used to embed a simple image in a webpage.
 In this article we'll look at how to use it in depth, including the basics,
 annotating it with captions using `<figure>`, and detailing how it relates to CSS background images.

How do we put an image on a webpage?
In order to put a simple image on a webpage, we use the `<img>` element. This is an empty element 
(meaning that it has no text content or closing tag)
 that requires a minimum of one attribute to be useful — src (sometimes spoken as its full title, source).
 The src attribute contains a path pointing to the image you want to embed in the page, which can be a relative or absolute URL,
 in the same way as href attribute values in <a> elements.

So for example, if your image is called dinosaur.jpg, and it sits in the same directory as your HTML page, you could embed the image like so:

`<img src="dinosaur.jpg">`

If the image was in an images subdirectory, which was inside the same directory as the HTML page (which Google recommends for SEO/indexing purposes), then you'd embed it like this:

`<img src="images/dinosaur.jpg">`

And so on.

Note: Search engines also read image filenames and count them towards SEO. Therefore, you should give your image a descriptive filename; dinosaur.jpg is better than img835.png.

You could embed the image using its absolute URL, for example:

`<img src="https://www.example.com/images/dinosaur.jpg">`

But this is pointless, as it just makes the browser do more work, looking up the IP address from the DNS server all over again, etc. You'll almost always keep the images for your website on the same server as your HTML.

Warning: Most images are copyrighted. Do not display an image on your webpage unless:

You own the image.
You have received explicit, written permission from the image owner.
You have ample proof that the image is, in fact, in the public domain.

Copyright violations are illegal and unethical. In addition, never point your src attribute at an image hosted on someone else's website that you don't have permission to link to. This is called "hotlinking". Again, stealing someone's bandwidth is illegal. It also slows down your page, leaving you with no control over whether the image is removed or replaced with something embarrassing.

Our above code would give us the following result:

![](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML/basic-image.png)

Alternative text

The easiest way to test your alt text is to purposely misspell your filename. If for example our image name was spelled dinosooooor.jpg, the browser wouldn't display the image, and would display the alt text instead:

![](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML/alt-text.png)

So, why would you ever see or need alt text? It can come in handy for a number of reasons:

The user is visually impaired, and is using a screen reader to read the web out to them. In fact, having alt text available to describe images is useful to most users.
As described above, the spelling of the file or path name might be wrong.
The browser doesn't support the image type. Some people still use text-only browsers, such as Lynx, which displays the alt text of images.
You may want to provide text for search engines to utilize; for example, search engines can match alt text with search queries.
Users have turned off images to reduce data transfer volume and distractions. This is especially common on mobile phones, and in countries where bandwidth is limited or expensive.
What exactly should you write inside your alt attribute? It depends on why the image is there in the first place. In other words, what you lose if your image doesn't show up:

Decoration. You should use CSS background images for decorative images, but if you must use HTML, add a blank alt="". If the image isn't part of the content, a screen reader shouldn't waste time reading it.
Content. If your image provides significant information, provide the same information in a brief alt text – or even better, in the main text which everybody can see. Don't write redundant alt text. How annoying would it be for a sighted user if all paragraphs were written twice in the main content? If the image is described adequately by the main text body, you can just use alt="".
Link. If you put an image inside <a> tags, to turn an image into a link, you still must provide accessible link text. In such cases you may, either, write it inside the same <a> element, or inside the image's alt attribute – whichever works best in your case.
Text. You should not put your text into images. If your main heading needs a drop shadow, for example, use CSS for that rather than putting the text into an image. However, If you really can't avoid doing this, you should supply the text inside the alt attribute.
Essentially, the key is to deliver a usable experience, even when the images can't be seen. This ensures all users are not missing any of the content. Try turning off images in your browser and see how things look. You'll soon realize how helpful alt text is if the image cannot be seen.

Width and height

You can use the width and height attributes to specify the width and height of your image. You can find your image's width and height in a number of ways. For example on the Mac you can use Cmd + I to get the info display up for the image file. Returning to our example, we could do this:

`<img src="images/dinosaur.jpg"`
     `alt="The head and torso of a dinosaur skeleton;`
          `it has a large head with long sharp teeth"`
     `width="400"`
     `height="341">`

This doesn't result in much difference to the display, under normal circumstances. But if the image isn't being displayed, for example, the user has just navigated to the page, and the image hasn't yet loaded, you'll notice the browser is leaving a space for the image to appear in:

![](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML/alt-text-with-width-height.png)

This is a good thing to do, resulting in the page loading quicker and more smoothly.

However, you shouldn't alter the size of your images using HTML attributes. If you set the image size too big, you'll end up with images that look grainy, fuzzy, or too small, and wasting bandwidth downloading an image that is not fitting the user's needs. The image may also end up looking distorted, if you don't maintain the correct aspect ratio. You should use an image editor to put your image at the correct size before putting it on your webpage.

Image titles

As with links, you can also add title attributes to images, to provide further supporting information if needed. In our example, we could do this:

`<img src="images/dinosaur.jpg"`
     `alt="The head and torso of a dinosaur skeleton;`
          `it has a large head with long sharp teeth"`
     `width="400"`
     `height="341"`
     `title="A T-Rex on display in the Manchester University Museum">`

This gives us a tooltip on mouse hover, just like link titles:

![](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML/image-with-title.png)


***


## Practical Information

Search Engine Optimization (SEO )

SEO is a huge topic and several books have been written on the subject.
The following pages will help you understand the key concepts so you can
improve your website's visibility on search engines.

The Basics
Search engine optimization (or
SEO) is the practice of trying
to help your site appear nearer
the top of search engine results
when people look for the topics
that your website covers.
At the heart of SEO is the idea of
working out which terms people
are likely to enter into a search
engine to find your site and then
using these terms in the right
places on your site to increase
the chances that search engines
will show a link to your site in
their results.
In order to determine who comes
first in the search results, search
engines do not only look at what
appears on your site. They also
consider how many sites link
to you (and how relevant those
links are). For this reason, SEO
is often split into two areas:
on-page techniques and off-page
techniques.

On-Page Techniques
On-page techniques are the
methods you can use on your
web pages to improve their
rating in search engines.
The main component of this is
looking at keywords that people
are likely to enter into a search
engine if they wanted to find
your site, and then including
these in the text and HTML code
for your site in order to help the
search engines know that your
site covers these topics.
Search engines rely very heavily
on the text that is in your pages
so it is important that the terms
people are going to search for
are in text. There are seven
essential places where you want
your keywords to appear.
Ensuring that any images have
appropriate text in the value of
their alt attribute also helps
search engines understand the
content of images.

Off-Page Techniques
Getting other sites to link to you
is just as important as on-page
techniques. Search engines help
determine how to rank your
site by looking at the number of
other sites that link to yours.
They are particularly interested
in sites whose content is related
to yours. For example, if you
were running a website that
sold fish bait, then a link from
a hairdresser is not likely to be
considered as relevant as one
from an angling community.
Search engines also look at the
words between the opening
<a> tag and closing </a> tag
in the link. If the text in the link
contains keywords (rather than
just click here or your website
address) it may be considered
more relevant.
The words that appear in links to
your site should also appear in
the text of the page that the site
links to.

## Video and Audio APIs

HTML5 comes with elements for embedding rich media in documents — <video> and <audio> — which in turn come with their own APIs for controlling playback, seeking, etc. This article shows you how to do common tasks such as creating custom playback controls.

HTML5 video and audio

The `<video>` and `<audio>` elements allow us to embed video and audio into web pages. As we showed in Video and audio content, a typical implementation looks like this:

`<video controls>`
  `<source src="rabbit320.mp4" type="video/mp4">`
  `<source src="rabbit320.webm" type="video/webm">`
  `<p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>`
`</video>`

The HTMLMediaElement API

Part of the HTML5 spec, the HTMLMediaElement API provides features to allow you to control video and audio players programmatically — for example HTMLMediaElement.play(), HTMLMediaElement.pause(), etc. This interface is available to both <audio> and <video> elements, as the features you'll want to implement are nearly identical. Let's go through an example, adding features as we go.

Implementing the JavaScript

We've got a fairly complete HTML and CSS interface already; now we just need to wire up all the buttons to get the controls working.

Create a new JavaScript file in the same directory level as your index.html file. Call it custom-player.js.

At the top of this file, insert the following code:

`const media = document.querySelector('video');`
`const controls = document.querySelector('.controls');`

`const play = document.querySelector('.play');`
`const stop = document.querySelector('.stop');`
`const rwd = document.querySelector('.rwd');`
`const fwd = document.querySelector('.fwd');`

`const timerWrapper = document.querySelector('.timer');`
`const timer = document.querySelector('.timer span');`
`const timerBar = document.querySelector('.timer div');`

Here we are creating constants to hold references to all the objects we want to manipulate. We have three groups:

The <video> element, and the controls bar.
The play/pause, stop, rewind, and fast forward buttons.
The outer timer wrapper <div>, the digital timer readout <span>, and the inner <div> that gets wider as the time elapses.
Next, insert the following at the bottom of your code:

`media.removeAttribute('controls');`
`controls.style.visibility = 'visible';`

Playing and pausing the video

Let's implement probably the most important control — the play/pause button.

First of all, add the following to the bottom of your code, so that the playPauseMedia() function is invoked when the play button is clicked:

play.addEventListener('click', playPauseMedia);
Now to define playPauseMedia() — add the following, again at the bottom of your code:

`function playPauseMedia() {`
  `if(media.paused) {`
    `play.setAttribute('data-icon','u');`
    `media.play();`
  `} else {`
    `play.setAttribute('data-icon','P');`
    `media.pause();`
  `}`
`}`

Here we use an if statement to check whether the video is paused. The HTMLMediaElement.paused property returns true if the media is paused, which is any time the video is not playing, including when it is set at 0 duration after it first loads. If it is paused, we set the data-icon attribute value on the play button to "u", which is a "paused" icon, and invoke the HTMLMediaElement.play() method to play the media.

On the second click, the button will be toggled back again — the "play" icon will be shown again, and the video will be paused with HTMLMediaElement.pause().

Stopping the video

Next, let's add functionality to handle stopping the video. Add the following addEventListener() lines below the previous one you added:

stop.addEventListener('click', stopMedia);
media.addEventListener('ended', stopMedia);
The click event is obvious — we want to stop the video by running our stopMedia() function when the stop button is clicked. We do however also want to stop the video when it finishes playing — this is marked by the ended event firing, so we also set up a listener to run the function on that event firing too.

Next, let's define stopMedia() — add the following function below playPauseMedia():

`function stopMedia() {`
  `media.pause();`
  `media.currentTime = 0;`
  `play.setAttribute('data-icon','P');`
`}`

there is no stop() method on the HTMLMediaElement API — the equivalent is to pause() the video, and set its currentTime property to 0. Setting currentTime to a value (in seconds) immediately jumps the media to that position.

All there is left to do after that is to set the displayed icon to the "play" icon. Regardless of whether the video was paused or playing when the stop button is pressed, you want it to be ready to play afterwards.

Seeking back and forth

There are many ways that you can implement rewind and fast forward functionality; here we are showing you a relatively complex way of doing it, which doesn't break when the different buttons are pressed in an unexpected order.

First of all, add the following two addEventListener() lines below the previous ones:

`rwd.addEventListener('click', mediaBackward);`
`fwd.addEventListener('click', mediaForward);`

Now on to the event handler functions — add the following code below your previous functions to define mediaBackward() and mediaForward():

`let intervalFwd;`
`let intervalRwd;`

`function mediaBackward() {`
  `clearInterval(intervalFwd);`
  `fwd.classList.remove('active');`

  `if(rwd.classList.contains('active')) {`
    `rwd.classList.remove('active');`
    `clearInterval(intervalRwd);`
    `media.play();`
  `} else {`
    `rwd.classList.add('active');`
    `media.pause();`
    `intervalRwd = setInterval(windBackward, 200);`
  `}`
`}`

`function mediaForward() {`
  `clearInterval(intervalRwd);`
  `rwd.classList.remove('active');`

  `if(fwd.classList.contains('active')) {`
    `fwd.classList.remove('active');`
    `clearInterval(intervalFwd);`
    `media.play();`
  `} else {`
    `fwd.classList.add('active');`
    `media.pause();`
    `intervalFwd = setInterval(windForward, 200);`
  `}`
`}`

You'll notice that first we initialize two variables — intervalFwd and intervalRwd — you'll find out what they are for later on.

Let's step through mediaBackward() (the functionality for mediaForward() is exactly the same, but in reverse):

We clear any classes and intervals that are set on the fast forward functionality — we do this because if we press the rwd button after pressing the fwd button, we want to cancel any fast forward functionality and replace it with the rewind functionality. If we tried to do both at one, the player would break.
We use an if statement to check whether the active class has been set on the rwd button, indicating that it has already been pressed. The classList is a rather handy property that exists on every element — it contains a list of all the classes set on the element, as well as methods for adding/removing classes, etc. We use the classList.contains() method to check whether the list contains the active class. This returns a boolean true/false result.
If active has been set on the rwd button, we remove it using classList.remove(), clear the interval that has been set when the button was first pressed (see below for more explanation), and use HTMLMediaElement.play() to cancel the rewind and start the video playing normally.
If it hasn't yet been set, we add the active class to the rwd button using classList.add(), pause the video using HTMLMediaElement.pause(), then set the intervalRwd variable to equal a setInterval() call. When invoked, setInterval() creates an active interval, meaning that it runs the function given as the first parameter every x milliseconds, where x is the value of the 2nd parameter. So here we are running the windBackward() function every 200 milliseconds — we'll use this function to wind the video backwards constantly. To stop a setInterval() running, you have to call clearInterval(), giving it the identifying name of the interval to clear, which in this case is the variable name intervalRwd (see the clearInterval() call earlier on in the function).

Finally, we need to define the windBackward() and windForward() functions invoked in the setInterval() calls. Add the following below your two previous functions:

`function windBackward() {`
  `if(media.currentTime <= 3) {`
    `rwd.classList.remove('active');`
    `clearInterval(intervalRwd);`
    `stopMedia();`
  `} else {`
    `media.currentTime -= 3;`
  `}`
`}`



`function windForward() {`
  `if(media.currentTime >= media.duration - 3) {`
    `fwd.classList.remove('active');`
    `clearInterval(intervalFwd);`
    `stopMedia();`
  `} else {`
    `media.currentTime += 3;`
  `}`
`}`

Again, we'll just run through the first one of these functions as they work almost identically, but in reverse to one another. In windBackward() we do the following — bear in mind that when the interval is active, this function is being run once every 200 milliseconds.

We start off with an if statement that checks to see whether the current time is less than 3 seconds, i.e., if rewinding by another three seconds would take it back past the start of the video. This would cause strange behavior, so if this is the case we stop the video playing by calling stopMedia(), remove the active class from the rewind button, and clear the intervalRwd interval to stop the rewind functionality. If we didn't do this last step, the video would just keep rewinding forever.
If the current time is not within 3 seconds of the start of the video, we remove three seconds from the current time by executing media.currentTime -= 3. So in effect, we are rewinding the video by 3 seconds, once every 200 milliseconds.



