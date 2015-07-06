---
tags: cssi, basic html
level: 1
languages: html
---
#HTML Basics

#Objectives:
+	Structure an html page using doctype, html, head and body tags
+	Explain what goes into the head of the document
+	Add text to a page using `p` and `h1` tags
+	Add images using img tag
+	Add links using `<a>` tags and understand the difference between relative and absolute paths
+	Create multiple pages and link them
+	Use styling tags like `<em>` `<strong>` `<div>` and `<span>`
+	Create lists with `ul`, `ol`, and `li`

#Why Should You Care?
HTML is the foundational technology for the Internet - every one of your favorite websites is HTML at its core. Today you are going to learn how to create an HTML site from scratch, and start creating a personal web page.

#Code-Along-Setup
1. Cmd+space: opens your spotlight search.
2. Type “Atom” and press enter
3. Go to “file” and click “new file” to open a new tab
4. Cmd+space Save as "hello_world.html"
5. Save the file on your desktop
6. Copy the boilerplate code below

```html
<!DOCTYPE html>
<title>My First Web Page</title>
Hello, world!
```
Save this somewhere on your local drive as hello.html. I like to use ~/Sites/project on OS X. You can view your site by opening it in Chrome.

Congratulations, you made a site! Obviously, there's a lot to do in order to make the site better. Let's get started by breaking down the different parts of what we wrote:
```html
<!DOCTYPE html>
```
This is -- reasonably enough -- called the DOCTYPE. It lets someone - or a program like your browser - know that the document it's looking at is an HTML document, and in particular, an HTML5 document. Browsers use this statement to determine whether your page should be displayed in "standards mode" (good) or "quirks mode" (old and inconsistent). It will make your life much easier if you remember to include this.
```html
<title>My First Web Page</title>
```
Note that this text doesn't appear on the body of the page, but in the title (which is usually in your browser's tab). It's important to make the title clear and succinct and contextually independent. This will also be the default bookmark name, and title of the search result for the page.
```html
Hello, world!
```
This is body text. It appears in the body of the page, where, and we haven't done anything extra to it other than make it appear in the browser window.

It turns out that there's a bit more going on behind the scenes. Sometimes, you'll see the same document written this way:
```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Web Page</title>
  </head>
  <body>
    Hello, world!
  </body>
</html>
```
In our version, the <html>, <head>, and <body> elements are all implied, since we  left them out. They let the browser know how to treat different elements on the page.

#Elements and Tags
HTML is made up of building blocks called "elements". You've already seen one, the <title> element. Elements are typically made up of an "opening tag", a "closing tag", and some content in between. Here's another example:
```html
<h1>All About Honey Badgers</h1>
```
This is an h1 (or "heading-1") element. Note that the opening tag <h1> differs from the closing tag </h1> by a slash.

Generally, elements are written like
```html
<tag>    .... CONTENT GOES HERE ....</tag>
```
They have an opening tag, then some content, and then a closing tag, which is a / and the tag name.

Elements can also have "attributes", which go inside the opening tag and give extra information about an element. For instance, on a link element, you might see this:
```html
<a href="http://www.google.com/">Search on Google</a>
```
Attributes take the form name="value". Here, we're linking to Google using an 'a' ("anchor") element. 'href' ("hypertext reference") indicates the site that should load when the user clicks on the link.

Different elements can have different attributes. For instance, links have hrefs, since they have destinations. Most elements cannot have hrefs. All elements, however, can have class and id attributes to help differentiate them from other elements.
```html
<h1 id="title">The Gettysburg Address</h1>

<p>Four score and seven years ago our fathers brought forth on this continent, a new nation, conceived in Liberty, and dedicated to the proposition that all men are created equal.</p>

<p class="about">Delivered by Abraham Lincoln on November 19, 1863.</p>
```
An id identifies a unique element on the page - there can only be one element that has that id.

The class lets us say that an element is a particular kind or group, used to identify and group elements that may occur more than once.

Some elements do not have closing tags; these are typically elements that have no textual content.

For example, the <img> element points to an image, but doesn't have any text inside.
```html
<img src="kittens.jpg" width="80" height="100" alt="Photo of kittens playing">
```
This tag has attributes (src, width, height, alt), but no closing tag.

#Tag Nesting
As you've seen, HTML elements just love to nest inside each other. This nesting is really useful for organizing the content of a page. On almost every page, there are pieces that belong to each other in a hierarchy.

For instance, a hierarchy of elements could be:
Text belongs to paragraphs, paragraphs belong to sections, sections belong to an article. Items in a list belong to a list, and the list can be a list of links in a nav bar. Both the article and the nav bar belong to the body of the page. The body of the page, the title, and some meta-info all belong to the whole html document.

```html
<html>
  <head>
    <title>Just an Example</title>
    <meta author="Helpful meta-info">
  </head>
  <body>
    <nav>
      <ol>
        <li>home</li>
        <li>another page</li>
        <li></li>
      </ol>
    </nav>
    <article>
      <h1>Article Title</h1>
      <section>
        <p>Here's some text!</p>
        <p>It's inside a paragraph inside a section</p>
        <p>inside an article inside the body inside the document</p>
      </section>
    </article>
  </body>
</html>
```
It's helpful to think about what parts of the page belong to each other, or are inside of one another. Then the html looks less like meaningless characters, and more like a useful way of structuring our documents!

#Whitespace
The browser mostly ignores the whitespace in your HTML page. If you have text on different lines or with lots of spaces in between, it will all get replaced by a single space. This is really helpful for making our HTML file readable - we can hit Enter as many times as we need to, and the browser will ignore it!

This:
```html
<p>For years, I wondered why Garfield was so popular. I still can't believe that anyone finds that cat funny in the slightest. It's mean to the man and dog. Ha.</p>
```
Will show up the same as this:
```html
<p>For years,

I wondered why Garfield was so popular.


I still can't                       believe that anyone finds that cat funny in the slightest. It's mean to the man and dog.


Ha.</p>
```
Why anyone would use the second one is beyond me, but there are lots of times when this trick can be useful!

It also forces us to use other ways to put whitespace into our pages, if we want it. We'll go in depth about styling and positioning when we cover CSS, but for now, there are two whitespace tricks to know.

br is the line break tag - it's like pressing enter on the keyboard.
```html
<p> I could use a <br> break</p>
```
&nbsp; is the html entity name for a no-break space. If you want to put extra spaces in between words, you can use it like this:
```html
<p> I need a little &nbsp; &nbsp; &nbsp; space </p>
```
#Types of Tags:
###Headers
Headers tell your visitors what your site is about. Usually, the main title of pages uses the `<h1>` tag.

Netflix might use headers like this:
```html
<!DOCTYPE html>
 <body>
   <h1>Netflix</h1>
   <h2>Top Picks For You</h2>
   <!-- your top picks would be here! --> 
  <h3>TV Shows</h3>
   <!-- TV Shows would be here! -->
   <h3>Comedies</h3> 
  <!-- Comedies here! -->
   <h3>Horror</h3>
   <!-- Horror Movies here! --> 
</body>
```

### Paragraphs and Emphasis
	1.	`<p>` tags, delineate paragraph text
	2.	`<strong>` will make any text contained within bold
	3.	`<em>` will italicize text or add emphasis

### Lists
	1.	Bullet point lists start with `<ul>` for unordered list
	2.	Numbered lists start with `<ol>` for ordered list
	3.	The actual list items go between `<li>` tags for, you guessed it, list items

```html
<ul>
   <li>item with bullet point</li>
   <li>2nd item with bullet point</li>
   <li>another list item</li> 
</ul>

  <ol>
   <li>Numbered item</li> 
  <li>List item #2</li> 
  <li>Third list item</li>
 </ol>
```
### Links
Links use an `<a>` tag, which stands for anchor. If you wanted a link to Google it would look like this:
`<a href="http://www.google.com">Super secret link</a>`

+ Images
Images use an `<img>` tag to embed an image in a webpage.
`<img src="your_image_location">`

#Indentation
HTML is not the easiest to read. It's designed to be clear for the browser to understand, but not always for humans. However, there are some ways to make it easier for you and others to read your code. Following the guidelines will help make your code easier to understand and debug.

Bad indentation:
```html
<html><head><title>The end of the world as we know it</title>
</head><body><p>
Some text about things</p></body>
```
This is confusing to read, and makes it harder to find errors. Can you spot the missing tag?

Good indentation:
```html
<html>
  <head>
    <title>
      The end of the world as we know it
    </title>
  </head>
  <body>
    <p>
      Some text about things
    </p>
  </body>
```
With better indentation, the missing tag is easy to spot!

#Comments

HTML also has a way to write things that won't show up in the browser at all. That doesn't sound very useful at first, but developers use this invisible text to leave helpful comments in the code.

HTML comments look like this:
```html
<!-- Here's a comment that won't get seen -->
<!--
Here's a comment that spans multiple lines!
See!
-->
```

Especially if you are doing something complicated, it's helpful to leave notes for yourself in your code. That way, if you came back a year later, or if someone else was reading your code and trying to understand it, they would have help!


#Conclusion
HTML allows us to define and label the content of our page. All modern browsers have implemented the same specification for how to display content written with html syntax. Now, you have control over how content is displayed, by naming the parts in the structure of your document.

#Personal Webpage Lab
Let's put all this into practice by building a personal webpage
<a href="https://github.com/learn-co-curriculum/cssi-1.4-html--personal-webpage-lab">Personal Webpage Lab</a>
