## HTML

Some of the fundamental HTML elements:
```html
<html> - represents the root of an HTML document
<head> - provides general information (metadata) about the document
<title> - defines the title of the document, shown in a browser's title bar
<link> - specifies relationships between the current document and an external resource
<body> - represents the content of an HTML document
<h1>, <h2>, ... Heading elements implement six levels of document headings
<p> - represents a paragraph of text
<div> - Division Element, generic container for flow content
<ol>, <ul> list of items with, or without numerical ordering
<li> - represents an item in a list
<a> - anchor element; defines a hyperlink to a location or page on the Web
<table> - display a data table. Note: not to be used for layout
<tr> - a table row
<td> - a cell in a table row
```

## CSS

There are three ways to add CSS rules to a page:
```html
Directly to an element. For example: <p style="color: red"></p>

Inline with HTML using a <style> tag. <style> tags usually go inside the <head> tag. An example is: <style> p { color: red; } </style>

Linking to a CSS file using a <link> tag. Here is an example of that tag: <link rel="stylesheet" href="style.css">
```


## ID vs Classes

IDs are used to identify unique elements on a page. Classes are used to indentify elements of the same type.

IDs are targeted with CSS using a hashtag prefix (ex. #buy-now-main-btn). Elements can only have 1 ID. 

Classes are targeted with a period/dot prefix (ex. .nav-item). Classes can be applied to as many elements as you want. Classes imply stylistic or behavioral properties about an element.
Classes should be used more frequently than IDs.

IDs can be used when you have a unique element taht is styled or behaves differently than other elements on the page. IDs are also used to reference them from the URL using the anchor hash value (ex. http://domain.com#comments with jump to the element with ID comments.)

Using IDs can give the browser slightly better performance because it only has to look for one element instead of every element with a certain class.


