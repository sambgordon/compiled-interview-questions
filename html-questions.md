<style>.head{ color: #d50c5a; }</style>
<style>.head-2{ color: #d50c5a; }</style>

# HTML Questions

<div class="head">

## What is HTML?

</div>

HTML is a markup language, and is used for creating websites that can be viewed in a web browser.


<div class="head">

## What is W3C?

</div>

W3C stands for World Wide Web Consortium. It serves as the international standard for the World Wide Web. It was created in 1994.


<div class="head">

## What does a **doctype** do?

</div>
 
It allows you to specify what version of HTML you're using.

`doctype` is an instruction to the browser informing it of the version of the HTML document, and how the browser should render it.
It ensures how elements should be displayed on the page by most of the browser.

It allows you to specify the `type` of a document, i.e., what kind of `HTML` document it is (`HTML5`, `XML`, etc).

It's used by the browser to tell user agents what version of HTML specifications your document uses.


<div class="head">

## What is **Quirks Mode**?

</div>
 
Basically **"Compatibility Mode"** - it means a relatively modern browser simulates bugs in older browser, esp. **IE 4 and 5**.
The purpose of `Quirks Mode` is to make old pages display as their author intended.

<div class="head">

## What multilingual considerations should you make?

</div>
 
* Use the `lang` attribute in your HTML.
* Allow a user to **change their country/language easily**.
* Also **consider language reading direction**.

<div class="head">


## What are **'data-'** attributes used for?

</div>
 
They were originally used to store data within the `DOM` itself, before Javascript frameworks became popular.
It's inteded to **store custom data private to the page/application**, for which there aren't more appropriate elements/attributes. These days, it's not typically encouraged.

They allow you to store extra info. in the DOM - you can write valid HMTL with embedded private data. They're accessed easily using Javascript.

<div class="head">

## What are the building blocks of **HTML5**?

</div>
 
* **New semantics** (able to more precisely describe your content).
* **Connectivity** - ability to communicate with the server
* 2D/3D graphics using `Canvas`, `SVG` and `OpenGL`.

<div class="head">

## What are some of the markup elements introduced in HTML5?

</div>

&lt;`nav`&gt;
&lt;`header`&gt;
&lt;`footer`&gt;
&lt;`section`&gt;
&lt;`bdi`&gt;

<div class="head">

## How would you create links to sections within the same page?

</div>

Links can be created using the &lt;`a`&gt; tag, using the # symbol to reference where to link to.



<div class="head">

## What's the difference between HTML elements and tags?

</div>

Elements communicate to the browser how to render text, and when surrounded by angular brackets they form HTML tags.

<div class="head">

## Define the difference between a "**cookie**" and "**sessionStorage**".

</div>
 
They're all on the client side, and are used to store information:

* A `cookie` is stored in the `browser`.
* A `session` is stored in the `server`.



<div class="head">

## What's the difference between a bulleted list and a numbered list?

</div>

&lt;`ul`&gt; - bulleted list. Stands for "unordered".
&lt;`ol`&gt; - numbered, ordered list.



<div class="head">

## What advantages does HTML5 offer over HTML?

</div>

* Better support for audio, video, and interactive graphics
* New semantics and markup
* Supports offline data storage for applications

<div class="head">

## What are some of the major APIs introduced in HTML5?

</div>

* Media API
* Data Transfer API
* History API

<div class="head">

## How does caching differ from HTML to HTML5?

</div>

HTML5 introduced the Application Cache, which creates an offline version of a web application. It stores files such as HTML, CSS, and JS files as well as images and does so locally.

<div class="head">

## What are the differences between &lt;**script**&gt;, &lt;**script async**&gt;, and &lt;**script defer**&gt;?

</div>
 
&lt;`script`&gt; is used to load a javascript file.
&lt;`script async`&gt; is to load _ajax_ to be available asynchronously
&lt;`script defer`&gt; - specifies a script to be run after page load

<div class="head">

## Why is it generally good to put CSS in the head tag, and JS script at the end of the body tag? Are there exceptions?

</div>
 
Since **HTML and CSS are parsed simultaneously**, this allows the CSS styles to load before everything else - HTML creates the `DOM`, and CSS creates the `CSSOM`. 

**Scripts block HTML parsing while being loaded**. If you put a script in the head, use the `defer` attribute.

An exception for scripts is when it contains `document.write()`, but nowadays that's typically bad practice to use document.write().


<div class="head">

## What is **Flash of Unstyled Content**? How do you avoid **FOUC**?

</div>

This occurs when a page's HTML loads before its CSS loads.

To prevent it, you can set the body section as having `<body style="visibility:hidden;" onload="js_load()">`, and writing a JS function `document.body.style.visibility='visible'`.

So to prevent FOUC you can force the page to be hidden until the full page, including the CSS files, are loaded.

<div class="head">

## Explain what **ARIA** and **screenreaders** are, and how to make a website accessible

</div>

**ARIA** stands for **Accessible Rich Internet Applications**. It defines attributes used to make web content more accessible to people with disabilities.

A **screenreader** reads text on a webpage aloud so a blind person can still use it.

<div class="head">

## Explain some of the pros and cons for **CSS animations** versus **JavaScript animations**.

</div>

CSS animations don't use your **CPU** and instead are optimized for **GPU** (**Graphics Processing Unit**) rendering. A disadvantage is that CSS transitions are very simplistic, although cover most use cases, while JS lets you customize your animations more.

<div class="head">

## What's **graceful degradation**?

</div>

**Graceful degradation** is the practice of building of building your website so it has a more advanced experience in modern browser, but also degrades gracefully to older browsers.

<div class="head">

## What's **progressive enhancement**?

</div>

**Progressive enhancement** is where you establish a basic level of user exxperience that all browsers can provide, and adds more advanced features that are automatically available to browser that can use it.

<div class="head">

## Can you describe the difference between **progressive enhancement** and **graceful degradation**?

</div>

They are very similar, however **graceful degradation** starts from complexity and **tries to fix the lesser experience**, whereas **progressive enhancement** starts from a basic working example and allows for constant extension for future environments. 

<div class="head">

## What is **progressive *rendering***?

</div>

**Progressive rendering** is a set of techniques used to **improve page load time** - so it's a form of **performance optimization**. Example:

**Lazy loading** of images - Javascript is used to load an image when a user scrolls to the part where it's displayed.


<div class="head">

## What is **DTD**?

</div>

DTD stands for Document Type Declaration. It tells the browser which version of HTML/XHTML to be used.

<div class="head">

## What advantages does **HTTP/2** offer compared to **HTTP 1.1**?

</div>

* Decreased latency
* Data compression of HTTP headers


<div class="head">

## What's a **marquee**?

</div>

A **marquee** is used to enable scrolling text in a web page. Anything you want to have appear as scrolling can be placed in between &lt;`marquee`&gt; tags.

<div class="head">

## What's the difference between a &lt;**div**&gt; and a &lt;**frame**&gt;?

</div>

A &lt;`div`&gt; is a container element for grouping and styling.
A &lt;`frame`&gt; creates divisions within a webpage, and should be used within the &lt;`frameset`&gt; tag.



<div class="head">

## Why would you use a **srcset** attribute in an image tag? 

</div>

`srcset` allows you to specify different kinds of images for different **screen sizes**, **orientations**, or **display types**.

So it can be thought of as an "image set".

<div class="head">

## How would you change the direction of **HTML** text?

</div>
 
The &lt;`bdo`&gt; element (**bidirectional override**).

<div class="head">

## How would you highlight text in **HTML**?

</div>
 
Use the &lt;`mark`&gt; element. 

<div class="head">

## What's the difference between **span** and **div?**

</div>
 
`Span` is **inline**, `div` occurs on a new line (`block`). +


<div class="head">

## What are cross-browser HTML5 elements?

</div>


## What's the advantage of collapsing white space?

White spaces are blank sequences of charactes. They're treated as a single character space in HTML. The browser **collapses multiple spaces into a single space**, so you can indent lines of text without worrying about multiple spaces. This allows you to organize code into a more readable format.





<div class="head">

## **Canvas** vs. **SVG**?

</div>

**Canvas** is:
* **Pixel-based**
* A single HTML element

**SVG** is:
* **Object-based**
* Multiple graphical elements (which become part of the **DOM**)

<div class="head">

## Explain the importance of **standards** and **standards bodies**.

</div>

<div class="head">

## What's **CORS** and how does it work?

</div>

**CORS** stands for **Cross-origin resource sharing**. It's a mechanism that allows many restricted resources to be requested from another domain outside the one it's originating from.

<div class="head">

## Can you list **DOM mouse events**?

</div>

**offsetX** - returns horizontal coordinate of mouse pointer relative to position of edge of target element

**offsetY** - returns vertical coordinate of mouse pointer relative to position of edge of target element

# **Performance**

<div class="head">

## Name 3 ways to **decrease page load** (perceived or actual load time)

</div>

* Minify files
* Minimize HTTP Requests
* Lazy loading

<div class="head">

## How would you optimize a website's assets/resources?

</div>

* Minify and combine files
* Reduce page size
* Automate repetitive tasks

<div class="head">

## If you have 5 different stylesheets, how would you best integrate them into the site?

</div>

I would combine them into one file, and if needed I would automate this process using something like Gulp.


<div class="head">

## How many resources will a browser download from a given domain at a time?

</div>

Firefox will download 6, Chrome will download 6, and IE11 will download 8.

<div class="head">

## What are common ways in which you can **reduce load time** of a web app?

</div>

* Enable browser caching so the computer saves some files, allowing future access to load more quickly
* Minify resources
* Optimize images - use SVG when possible
* Minimize number of HTTP Requests

# General


<div class="head">

## Are you familiar with the process of **pull requests**?

1. **Fork** the repo
2. **Build** or clone the repo to your machine
3. Create **new branch**
4. Make changes
5. **Commit**
6. **Push**
7. Open Pull Request
8. Discuss and Update

</div>

<div class="head">

## Can you explain **version control**?

</div>

**Version control** is a process where you keep a software system that has various verisons and configurations organized. 

Git and Github let you use repos that allow you to create new branches and open a pull request for changes you make on the new branch.