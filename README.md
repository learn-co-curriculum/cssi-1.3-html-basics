---
tags: cssi, basic html
level: 1
languages: html
---
#HTML Basics

#Prior Knowledge:
+ Intro to the web
+ Github account setup
+ Learn.co walkthrough

#Student Objectives:
  + Structure an html page using doctype, html, head and body tags
  + Explain what goes into the head of the document
  + Add text to a page using p and h1 tags
  + Add images using img tag
  + Add links using <a> tags and understand the difference between relative and absolute paths
  + Create multiple pages and link them
  + Use styling tags like <em><strong><div> and <span>
  + Create lists with ul, ol, and li
  + Understand best practices for tag nesting
  + Understand how to make comments
  + Understand how the browser reads whitespace in HTML

#Motivation
HTML is the foundational technology for the Internet, every one of your favorite websites is HTML at its core. Today you are going to learn how to create an HTML site from scratch. And create your own styles for your personal web page.

#Code-Along-Setup
1. Cmd+space: opens your spotlight search.
2. Type “Atom” and press enter
3. Go to “file” and click “new file” to open a new tab
4. Cmd+space Save as "practice.html"
5. Save the file on your desktop
6. Copy the boiler plate code below

```
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

#Tag syntax and attributes
HTML is made up of building blocks called "elements".
```
<tag> .... CONTENT GOES HERE .... </tag>
```
Attribute: Different elements can have different attributes. All elements can have class and id attributes to help differentiate them from other elements.

```
<h1 id="title">The Gettysburg Address</h1>
<p class="about">Delivered by Abraham Lincoln on November 19, 1863.</p>
```
+ ID - identifies a unique element on the page and there can only be one element that has that id.
+ Class- Identifies and group elements that may occur more than once.

#Tag Nesting and Whitespace
The browser mostly ignores the whitespace in your HTML page.

br is the line break tag - it's like pressing enter on the keyboard.
```
<p> I could use a <br> break</p>
```
&nbsp; is the html entity name for a no-break space. If you want to put extra spaces in between words, you can use it like this:
```
<p> I need a little &nbsp; &nbsp; &nbsp; space </p>
```

#Types of Tags:
+ Headers
Headers tell your visitors what your site is about. Usually, the main title of pages uses the `<h1>` tag.

Netflix might use headers like this:
```
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

+ Paragraphs and Emphasis
	1.	`<p>` tags, delineate paragraph text
	2.	`<strong>` will make any text contained within bold
	3.	`<em>` will italicize text or add emphasis

+ Lists
	1.	Bullet point lists start with `<ul>` for unordered list
	2.	Numbered lists start with `<ol>` for ordered list
	3.	The actual list items go between `<li>` tags for, you guessed it, list items

```
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
+ Links
Links use an `<a>` tag, which stands for anchor. If you wanted a link to Google it would look like this:
`<a href="http://www.google.com">Super secret link</a>`

+ Images
Images use an `<img>` tag to embed an image in a webpage.
`<img src="your_image_location">`

#Indentation and Nesting
HTML is not the easiest to read. It's designed to be clear for the browser to understand, but not always for humans. Indentation help make your code easier to understand and debug.

No indentation:
```
<html><head><title>The end of the world as we know it</title>
</head><body><p>
Some text about things</p></body>
```
This is confusing to read, and makes it harder to find errors. Can you spot the missing tag?

Indentation:
```
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
```
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
You are now ready to add html onto your personal webpage lab
<a href="https://github.com/learn-co-curriculum/cssi-1.4-html--personal-webpage-lab">Personal Webpage Lab</a>
