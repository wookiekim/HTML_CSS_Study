# Chapter 1 : Structure

### HTML describes the structure of pages

HTML code is made up of characters that live inside angled brackets called HTML **elements**.
* Elements are made up of two tags:
  1. opening tag (ex `<html>`)
  2. closing tag (ex `</html>`)
    * The closing tag has an extra forward slash (/) 
* Tags act like containers. A few examples:
  * `<html>` indicates anything within this tag is HTML code
  * `<body>` indicates anything within this tag should be shown inside the main browser window
  * `<h1>` indicates main heading.
  * `<p>` indicates paragraph
  * `<h2>` indicates sub-heading

Attribute provide additional information about the contents of an element
* Appear on the opening tag of the element
* Made up of two parts:
  1. name (should be written in lowercase)
  2. value (should be placed in double quotes)
* ex) `<p lang="en-us"> Paragraph is English </p>`
  * 'lang' is attribute name, 'en-us' is attribute value
* Majority of attributes can only be used on certain elements
  * A few elements (such as 'lang') can appear on any element

`lang attribute is an abbreviated way of specifying which language is used inside the element`

### Body, Head & Title

1. `<body>`
Everything inside this element is shown inside the main browser window
2. `<head>`
Contains information *about* the page rather than information shown *within* the browser.

Usually a `<title>` element will be found inside the **<head>** element.
3. `<title>`
Shown in the top of the browser, above where the URL **or** on the tab for that page.

`HTML stands for HyperText Markup Language`

`Use TextEdit in Mac as a replacement for Notepad`

To learn about HTML tips and techniques: 
* Look at the source code that made  up the pages
* [View source] option (chrome F12)

### Summary
* HTML pages are text documents
* HTML uses tags which act like containers and tell you something about the information that lies between them
* Tags are AKA elements
* Tags come in pairs (opening, closing tag)
* Opening tags can carry attributes, which tell us more about the content of that element
* Attributes require a name and a value
* To learn HTML you need to know:
  * WHAT tags are available for you to use
  * WHAT each tag does
  * WHERE they can go
