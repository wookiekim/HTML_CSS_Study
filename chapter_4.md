# Chapter 4 : Links

You will commonly come across the following types of links:
* Links from one website to another
* Links from one page to another on the same website
* Links from one part of a web page to another part of the same page
* Links that open in a new browser or window
* Links that start up your email program and address a new email to someone

Links are created using the `<a>` element.
* The page you want to link to is specified by the `href` attribute.
  * ex) `<a href="http://www.imdb.com">IMDB</a>`
* Users can click on anything between the opening and closing tag of `<a>`
  * known as link text

### Different types of links

When linking to other site: **Absolute URL** should be in the `href` attribute.

When linking to other pages on the same site: **Relative URL** can be used.
* in the code examples, `index.html` files contains links that use relative URLs.
* Possible because pages of the same site are usually in the same folder.
  * In this case can just use the file name for that page
* If in differnt folder, jsut like in terminal
  * Name of directory for child(or grandchild..) folders
  * `../` for parent folders
```
Directory Structure

Good idea to place pages of different sections of the website in different folders
- which are also known as directories

Top-level folder is known as the ROOT folder.
Relationship between folders can be defined by parent-child relationships

The main homepage is called index.html
- Web servers are usually set up to return index.html if no file name is specified.

If using a content management system, blogging software or en ecommerce system,
you might note have individual files for each page of the website

These use templates instead, and editing the template file would
change all the pages that use that template
```

`"mailto:jon@example.org"` as `href` attribute for Email links.

Use the `target` attribute to open links in a new window.
* `<a href="(url)" target="_blank">asdf</a>`
* may open in new tab depending on the browser

Use the `id` attribute to link to specific part of the same page
* should begin with a letter or underscore
* on the same page, no two id attributes should have the same value
* Use link in a way `<a href="#(id attribute value)">` to link to the corresponding part of the page holding that 'id value'.

When linking to a specific part of another page, it is similar:
* `<a href="(url)#(id attribute value)">`

### Summary
* Links are created using the `<a>` element
* The `<a>` element uses the href attribute to indicate the page you are linking to
* If you are linking to a page within your own site, it is best to use relative links rather than qualified URLs
* You can create links to open email programs with an email address in the "to" field
* You can use the id attribute to target elements within a page that can be linked to.
