# Chapter 10 : Introducing CSS

Key to understanding CSS: 
> Imagine there is an invisible box around EVERY HTML element.
> CSS allows you to create rules that control the way each individual box (and its contents) is presented.

Block elements
* look like they start on a new line
* `<h1>`, `<p>`, `<div>` ...

Inline elements
* Flow within the text
* Do not start on a new line
* `<em>`, `<span>`...

CSS works by associating rules with HTML elements. CSS rule contains two parts:
1. Selector
  * indicate which HTML element the CSS rule applies to.
  * Same rule can be applied to more than one element if the **element names are separated with commas**
2. Declaration
  * indicate how the elements referred should be styled
  * Separated by a colon
  * Made up of 1.Property, 2.Value
    * Property indicate the aspects of the element to be changed (color, font, width, height..)
    * Values specify the settings you want to use for the chosen property

Looks somewhat like:
```html
h1, h2, h3 { 
	   font-family: Arial;
	   color: yellow;}
```
`h1,h2,h3 :: Selector`
`font-family, color :: Property`
`Arial, yellow :: Value`


`<link>` element can be used to tell the browser where to find the CSS file (external CSS)
* usually inside the `<head>` element
* `href` attribute to specify the path to CSS file
* `type` attribute to specify type of document being linked to (has to be `text/css` in this case)
* `rel` attribute to specify relationship between HTML page and the file. 
  * has to be `stylesheet` when linking to a CSS file.
* A HTML page can use more than one CSS style sheet.
  * needs `<link>` for every CSS stylesheet it uses.

Looks like:
```
<head>
  <title>---</title>
  <link href="css/example.css" type="text/css" rel="stylesheet" />
<head>
```

`<style>` element for internal css (include CSS rules within an HTML page)
* usually inside the `<head>` element
* should also use `type` attribute to specify type of document being linked to (has to be `text/css` in this case)

WHen building a site with more than one page, advised to use an external CSS style sheet.
* Allows all pages to use the same style rules
* Keeps the content separate from how the page looks
* Means you can change the styles used across all pages by altering just one file (rather than each individual page)

```
In older HTML, a 'style' attribute could be used on individual elements.

ex) <p stule="color:red;">

Should avoid this on new sites, but may still be seen in older websites.
```

### CSS Selectors
Allows to target rules to specific elements in an HTML documents.

Selectors are Case sensitive, so they must match element names and attribute values exactly.

More advanced Selectors [here](Chapter 12).

1. Universal Selector
Applies to all elements in the document 
* ex) `* {}`
2. Type Selector
Matches element names 
* ex) `h1, h2 {}`
3. Class Selector
Matches an element whose *class* attribute has a value that matches the one specified after the **period** symbol 
* ex1) `.note {}` targets any element whose class attribute has a value of "note"
* ex2) `p.note {}` targets only `<p>` elements whose class attribute has a value of "note"
4. ID selector
Matches an element whose *id* attribute has a value that matches the one specified after the pound or hash symbol
* ex) `#introduction {}` targets the element whose id attribute has a value of "introduction"
5. Child Selector
Matches an element that is a direct child of another
* ex) `li>a {}` targets any `<a>` elements that are children of `<li>` element
6. Descendant Selector 
Matches an element that is a descendent of another specified element (not just a direct child of that element)
* ex) `p a {}` targets any `<a>` elements that sit inside a `<p>` element, even if there are other elements nested between
7. Adjacent Sibling Selector
Matches an element that is the next sibling of another
* ex) `h1+p {}` targets the first `<p>` element after any `<h1>` element (but not other `<p>` elements)
8. General Sibling Selector
Matches an element that is a sibling of another, although it does not have to be the directly preceding element.
* ex) `h1~p {}` If you had two `<p>` parents that are sibling of an `<h1>` element, this rule would apply to both.

### How CSS Rules cascade
If two or more reuls apply to the same element, which one takes precedence?

***Last Rule***
> If two selectors are identical, the latter of the two will take precedence. 

***SPECIFICITY***
> If one selector is more specific than the others, the more specific rule will take precedence over more general ones.
> ex) `h1` is more specific than `*`
> ex) `p b` is more specific than `p`
> ex) `p#intro` is more specific than `p`

***IMPORTANT***
> You can add `!important` after any **property** value to indicate that it should be considered more important than other rules that apply to the same element.

### Inheritance

The **font-family** or **color** properties on the `<body>` element will apply to most chlid elements
* **font-family** property is inherited to child elements
  * Saves the fuss of having to apply these properties to as many elements
  * Results in simpler stylesheets

**background-color** or **border** properties are not inherited.

You can **force** "a lot of" (quite vague, I think) properties to inherit values from their parent elements by using `inherit` for the value of properties.

Somewhat like:
```CSS
.page {
  border: 1px solid #665544;
  background-color: #efefef;
  padding: inherit;}
```

### CSS & Browser quirks
Before launching any new site, important to test in more than one browser
* may differ in how it is displayed by each browser
* Online tools to show what a page looks like in multiple browsers:
  * [BrowserCam.com](BrowserCam.com)
  * [BrowserLab.Adobe.com](BrowserLab.Adobe.com)
  * [BrowserShots.org](BrowserShots.org)
  * [CrossBrowserTesting.com](CrossBrowserTesting.com)
* should check on different OS, different version of same browser...

Browser Quirk / CSS bug :: when a CSS property does not display as expected.

Check these sites upon coming across a CSS bug:
* [PositionIsEverything.net](PositionIsEverything.net)
* [QuirksMode.org](QuirksMode.org)

### Summary
* CSS treats each HTML element as if it appears inside its own box and uses rules to indicate how that element should look.
* Rules are made up of selectors (that specify the elements the rule applies to) and declarations (that indicate what these elements should look like)
* Different types of selectors allow you to target your rules at different elements
* Declarations are made up of two parts: the properties of the element that you want to change, and the values of those properties. For example, the font-family property sets the choice of font, and the value arial specifies Arial as the preferred typeface. 
* CSS rules usually appear in a separate document, although they may appear within an HTML page.
