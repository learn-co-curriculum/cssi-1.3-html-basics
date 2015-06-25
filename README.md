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
HTML is the foundational technology for the Internet, every one of your favorite websites is HTML at its core. Today you are going to learn how to create an HTML site from scratch. And create your own styles for your personal web page.

#Code along Setup
+	`Cmd+space`: opens your spotlight search.
+	Type `Terminal` and press enter: opens your command line
+	`mkdir development`: Creates the “development” directory where you will keep all of your projects
+	`cd development`: goes inside development directory
+	`mkdir my_website`: creates a directory called “my_website”
+	`cd my_website`:goes inside “my_website”
+	`mkdir css`: creates a css directory “my_website”
+	`touch index.html`: creates a html file inside “my_website”
+	`subl index.html`: Opens index.html in sublime
+	```
<!doctype html>
<html>
  <head>
  </head>
   <body>
  </body>
</html>
```: You now have an empty html page!

#Tag syntax
```<tag> .... CONTENT GOES HERE .... </tag>```
Tags can also have attributes applied to them. These can be thought of as modifying or providing additional information to a tag.
<tag attribute="attribute value">  .... CONTENT GOES HERE .... </tag>

#Tag Nesting and Whitespace

Bad indentation
<html><head><title>The end of the world as we know it</title> </head><body><p> Some text about things</p></body>
This is not only confusing but can also make it harder to find errors. Can you spot the missing tag?

Good indentation
<html>   <head>     <title>       The end of the world as we know it     </title>   </head>   <body>     <p>       Some text about things     </p>   </body>


Types of Tags:
Headers
Headers tell your visitors what your site is about. Usually, the main title of pages uses the <h1> tag.

Netflix might use headers like this:

<!DOCTYPE html> <body>   <h1>Netflix</h1>   <h2>Top Picks For You</h2>   <!-- your top picks would be here! -->   <h3>TV Shows</h3>   <!-- TV Shows would be here! -->   <h3>Comedies</h3>   <!-- Comedies here! -->   <h3>Horror</h3>   <!-- Horror Movies here! --> </body>

Other Tags
	•	<p> tags, delineate paragraph text
	•	<strong> will make any text contained within bold
	•	<em> will italicize text or add emphasis

Lists
	•	Bullet point lists start with <ul> for unordered list
	•	Numbered lists start with <ol> for ordered list
	•	The actual list items go between <li> tags for, you guessed it, list items
<ul>   <li>item with bullet point</li>   <li>2nd item with bullet point</li>   <li>another list item</li> </ul>  <ol>   <li>Numbered item</li>   <li>List item #2</li>   <li>Third list item</li> </ol>

Links
Links use an <a> tag, which stands for anchor. If you wanted a link to Google it would look like this:
<a href="http://www.google.com">Super secret link</a>

Images
Images use an <img> tag to embed an image in a webpage.
<img src="your_image_location">

Conclusion / So What?
HTML allows us to define and label the content of our page. All modern browsers have implemented the same specification for how to display content written with html syntax. Now, you have control over how content is displayed, by naming the parts in the structure of your document.
