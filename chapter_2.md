# Chapter 2 : Text

**Structural Markup**
* elements that describe both headings and paragraphs

**Semantic markup**
* Provides extra information such as:
  * where emphasis is placed in a sentence
  * something you have written is a quotation (and who said it)
  * Meaning of acronyms..etc

### Headings
HTML has six levels of headings:
h1 ~ h6

* `<h1>` for main headings
* `<h2>` for subheadings
* and further subheadings..

The size at which each browser shows the headings can vary slightly.
* CSS will allow control of size of text, color, and fonts used

### Paragraphs
`<p>` tag

By default, browser will show each paragraph on a newline with some space between it and any subsequent paragraphs.

### Bold & Italic

`<b>` for Bold

`<i>` for italic

### Superscript & Subscript

`<sup>` for superscript (above)

`<sub>` for subscript (below)

```
White space collapsing?

When the browser comes across two or more spaces next to each other,
it just displays one space.

Similarly if it comes across a line break,
the line break is treated as a single space.

This may be exploited to indent code for better readability.
```

### Line breaks & Horizontal Rules 

`<br />` tag for line break
* can be used between paragraph tags (`<p>`)

`<hr />` tag for horizontal rule

```
Empty elements?

No words between opening and closing tag
Usually has only one tag (above 2 included)
The space and forward slash (' /') is a good habit to use
```

```
Visual Editors?

ex) Dreamweaver
Has two view of the page being created:
A visual editor and a code view.

(Download Dreamweaver?)
```
### Semantic Markups

Text elements not intended to affect that structure of web pages
but DO add extra information to the pages


`<strong>` indicates its content has strong importance. 
* By default, shown in **bold**

`<em>` indicates emphasis that subtly changes the meaning of a sentence
* By default, shown in *italics*

`<blockquote>` used for longer quotes that take up an entire paragraph. 
* the paragraph tag `<p>` should still be used inside the `<blockquote>` tag.
* Can use "cite" attribute, with value containing the URL to source of quote.

`<q>` for shorter quotes that sit within a paragraph.
* By default, double quoted.
* Can also use the "cite" attribute

`<abbr>` for abbreviations, or acronyms.
* May use "title" attribute to refer to full form of abbreviation.

`<cite>` when referencing a piece of work such as a book, film, or research paper.
* By default, shown in *italics*

`<dfn>` to indicate the defining instance of a new term.
* By default (not in chrome or Safari..thus near obsolete?) shown in *italics*

`<address>` to contain contact details for the author of the page
* may search for [hCard microformat] to add physical address information to my markup.

`<ins><del>` elements to show text that has been inserted, and deleted.
* Frequently seen in namuwiki, something like ~~thsi~~_this_
* By default, `<ins>` is underlined, while `<del>` has a strikethrough.

`<s>` indicates something that is no llonger accurate of relevant, but should not be deleted.
* By default, has a ~~strikethrough~~

## Summary
* HTML elements are used to describe the structure of the page
* They also provide semantic information (e.g where emphasis should be placed)
