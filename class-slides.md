HTML/CSS
======

Introduction to Web Development
------

About Me
======

* Instructor : Kevin Sholander
* Email : kevin@learningfuze.com

Agenda
======
1. [Introductions](#introductions)
2. [Web Overview](#weboverview)
3. [Development Environment](#environment)
4. [HTML Foundations](#htmlfoundations)
5. [CSS Foundations](#cssfoundations)
6. [Project](#project)
7. [Tools](#tools)
8. [Website Creation Checklist](#checklist)
9. [Next Step Possibilities](#nextsteps)
10. [Resources](#resources)

<a name="introductions"></a>Introductions
======

<a name="weboverview"></a>Web Overview
======
## Client / Server Architecture
![client server web architecture](https://github.com/ksholander/Intro-Class-Project-2-21/blob/master/images/client_server.png?raw=true)
* **Client**
  * Renders pages within a browser
  * Stores small amounts of local data in cookies or local store
  * Executes client side scripts within browser sandbox
* **Server**
  * Runs web server software such as Apache
  * Responds to requests by sending pages (HTML) and images
  * Executes server side scripts to generate custom page content
  * Able to store large amounts of data in server database

## Anatomy of a Web Page
* **HTML _(HyperText Markup Language)_** - Carries the page content
  * Text
  * Hyperlinks
  * Images (actually links to images)
  * Markup language, not programming language
* **CSS _(Cascading Style Sheets)_** - Describes the page appearance
  * Rules that pair content with style
  * Allows different rules for different media (small screens, large screens, printers, etc)
* **JavaScript** - Programs the page behavior
  * A C-like object based programming language
  * Runs within the browser
  * Can be used to define navigation behavior, validate form inputs, and control page animations
* **Website** - A bunch of web pages glued together with hyperlinks

## Examples
  * [Google](http://www.google.com)
  * [Yahoo](http://www.yahoo.com)
  * [Tumblr](https://www.tumblr.com)
  * [CSS Zen Garden](http://www.csszengarden.com)

<a name="environment"></a>Development Environment
======
## Browser (obviously)
* Chrome

  Open source browser developed by Google. Available across most platforms (Windows, iOS, Linux). Includes very powerful debugging tools for developers. This browser enjoys the largest marketshare amongst all browsers and is a good choice for primary development.
* Firefox

  Open source browser developed by Mozilla (based on the old Netscape Navigator). Plugin developer tools are available. Runs on most platforms. Second most popular browser after Chrome. Make sure to test all of your websites in both Chrome and Firefox at a minimum.
* Safari

  Apple's native browser, also available for Windows and Linux machines. This browser is not very popular outside of Apple machines, but with the popularity of iPhones, it is especially important to test on this browser when designing sites targeted at mobile devices.
* Internet Explorer

  Microsoft's browser, which now includes fairly decent developers tools. Due to continuous deliberate inconsistancies programmed into the browser (mostly to increase MS competitive advantage), this browser has fallen out of favor with most users and developers. Still controls about 15% market share, so cannot be overlooked entirely.
## Text editor (__NOT__ Wordprocessor)
* [Brackets](http://brackets.io)

  Designed specifically for web development using web technology. Much more than just a text editor, this tool integrates CSS style previews, JS lint checking, page previewer and debugger, and source code management all into one Integrated Development Environment (IDE).
* [Sublime Text](http://www.sublimetext.com)

  Free download for evaluation. License requires purchase for continued use.
* [Notepad++](http://notepad-plus-plus.org)

  Free, open source editor for MS Windows machines
* [Vim](http://www.vim.org)

  An improved version of the vi editor that ships with most UNIX/LINUX systems. Very powerful and flexible editor with a very steep learning curve. Not for the faint of heart.
* Notepad - junk. Do not use
## Debuggers

   A debugger is a tool that helps developers by exposing the inner workings of the scripts, HTML, and CSS, so that problems, odd behaviors, and bugs can be easily tracked down and fixed
## Server Software and Database

   In order to fully test the behavior of a website, it is important to see how the site will perform on an actual server. Depending on your development machine, LAMP (Linux), WAMP (Windows), or MAMP (iOS), are available as open source, free downloads. These applications convert your computer into a fully functional, Apache based web server with MySQL database.

## Setting Up Your Environment

* If you don't have it already, download and install [Chrome](http://www.google.com/chrome)
* Download and install [Brackets](http://brackets.io)
* Setup a root folder to store your work
  * On your desktop create a folder named "sandbox"
  * In the "sandbox" folder:
    * Create a folder called "HTMLpractice"
    * Create a folder called "CSSpractice"
    * Create a folder called "project1"

<a name="htmlfoundations"></a>HTML Foundations
======
## What is HTML?
  * _H_yper_T_ext _M_arkup _L_anguage
  * HyperText - active text that performs an action when clicked, such as a link or a button
  * Markup - markers are added to the content to indicate to the browser the intent of the content
  * Language - The language is based on standards that are defined and maintained by the [W3 consortium](http://www.w3.org)
  * Current revision is HTML5
  * Older versions : HTML, XHTML, HTML4

## Creating an HTML document
  * Document must consist of only simple text (do not use a word processor to create or edit an HTML file)
  * Filename should end with ".html" or ".htm" to indicate that it contains an html document
  * Filename must not have spaces, i.e. use "filename.html" not "file name.html"
  * First line should be "<!DOCTYPE html>". This tells the browser that the file contents are compatible with the HTML5 standard
  * The rest of the document consists of elements

## What is an HTML element?
  * An element consists of a tag, optional attributes, the element contents, and a closing tag
  * The tag indicates the intent of the content
  * Tags are case insensitive, but it is considered best practice to always use lower case
  * Most, but not all, elements require a closing tag
  * An element may contain other elements

  * Examples:

```
    <p>This is a paragraph</p>
```

    Note:  
    The tag is contained within angled brackes "<" and ">".  
    The closing tag is the same as the tag but has an extra slash "/"
    The contents are all of the text that is between the opening tag and the closing tag

```
    <h1 id='header1'>This is a header</h1>
```

    Note:  
    The optional attributes have information about the element.  
    Neither the tag nor the attributes will appear in the rendered page.  
    They may, however, change _how_ the element will be displayed in the rendered page.
    Attributes are specified as _name="value"_ and are located within the opening tag.  
    Some tags require attributes to be set. See [w3schools tag specification](http://www.w3schools.com/tags/tag_p.asp) for information about specific tags.

```
    <p>This paragraph contains <strong>BOLD</strong> characters</p>
```

    Note:  
    Elements can be contained within other elements.  
    Nested elements must have their closing tag _before_ the closing tag of the element they are contained within.

```
    <img src='url/of/some/image.jpg' />
```

    Note:  
    Some elements are "self closing".  
    Self closing elements do not require a closing tag. Instead they have a slash before the closing angled bracket "/>"
    Self closing tags may contain attributes but never have any content.

## Try It!

* Open Brackets
* Drag the "sandbox" folder from your desktop and drop into the project browser panel (left side, dark gray portion) of brackets
* Right click on "HTMLpractice" in the Brackets project browser panel and select "New File"
* Rename the new file to "skeleton.html". The file will automatically open in the editor window (large white window on the right)
* Type the following code into the editor window. Note that the editor will assist you by autoclosing your tags and indenting

```
<!DOCTYPE html>
<html>
    <head>
        <title>Skeleton HTML</title>
    </head>
    <body>
    </body>
</html>
```
* Open the file in your browser (click the lightning bolt on the right side of brackets)

## Some useful tags
* html

  The entire page must be contained within an html element.

* head

  The head element is the first element within the html page. It contains inoformation about the page, such as title, links to scripts and css, metadata to aid search engines, etc.

* title

  The title is the only required element within the head. It contains the title of the document which appears in the tab at the top of the browser and is used by search engines to figure out what the page is about.

* body

  The body element is required immediately after the head. The body contains all of the elements that will be displayed in the browser.

* h1, h2, h3, h4, h5, h6

  Header elements are used to mark the headers within a page. These elements are usually displayed with larger, bold and possibly underlined text. They are also used by search engines to help determine what information on the page is important for cataloging.

* p

  Paragraphs are blocks of text that are separated from other blocks of text.

* img

  Image tags must contain a src attribute which is a url that points to the image file.

* strong, em
  A strong tag indicates text that should appear strongly (as in bold). The em tag indicates text that should be emphasized (as in italics).

* ul, ol
  An unordered list is a bullet list. An ordered list is a numbered list. ul and ol elements may only contain list item elements (li). They may not contain paragraphs, headers, images or any other type of tag. Of course, a list item element may contain images or other element types.

* li
  A list item must be contained within an unordered (ul) or ordered (ol) list.


## Sample page

```
<!DOCTYPE html>
<html>
  <head>
    <title>Sample Page</title>
  </head>
  <body>
    <h1>First Webpage</h1>
    <p>This is my <strong>first webpage</strong>.  I am so proud of it.</p>
    <h2>Here is a numbered list</h2>
    <ol>
      <li>This is the <em>first</em> item</li>
      <li>This is the <em>second</em> item</li>
      <li>This is the <em>third</em> item</li>
    </ol>
    <h2>Here is a bullet list</h2>
    <ul>
      <li>This is the <em>first</em> item</li>
      <li>This is the <em>second</em> item</li>
      <li>This is the <em>third</em> item</li>
    </ul>
    <h2>Here is an image</h2>
    <img src="https://github.com/ksholander/Intro-Class-Project-2-21/blob/master/images/client_server.png?raw=true" width="400" height="200" />
  </body>
</html>

##

<a name="cssfoundations"></a>CSS Foundations
======

<a name="project"></a>Project
======

<a name="tools"></a>Tools
======

<a name="checklist"></a>Website Creation Checklist
======

<a name="nextsteps"></a>Next Step Possibilities
======
* [Frontend Development Course](http://learningfuze.com/frontend-development) - 
* [Full Stack Immersive Bootcamp](http://learningfuze.com/program-overview) - 
* [Career Potential in Web Development](http://learningfuze.com/why-coding) - explore why web development might be a great career choice for you
* [W3 Schools](http://www.w3schools.com) - free, self-paced, online learning courses in HTML, CSS, JavaScript, SQL, PHP, jQuery and more
* [Code School](http://www.codeschool.com) - web based, self-paced training. Teach yourself

<a name="resources"></a>Resources
======
* [W3C Markup Validator](http://validator.w3.org) - check the validity of your HTML markup
* [W3 Schools](http://www.w3schools.com) - web standards, language reference, tutorials
* [GitHub](http://www.github.com) - Repository for maintaining version control of your work and sharing files with others
* [JSFiddle](http://jsfiddle.net) - Online tool for testing and sharing client side code (html, css, javascript)
* [JSHint](http://jshint.com) - JavaScript code quality tool
* [TutsPlus](http://tutsplus.com) - Blog and tutorials to help you keep up with the latest in web development techniques and best practices

