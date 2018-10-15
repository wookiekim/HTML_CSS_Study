# Chapter 3 : Lists

Three different types of lists in HTML:
1. Ordered lists (numbered)
2. Unordered lists (bullet points)
3. Definition lists
  * made up of set terms along with definitions for each of thsoe terms

### Type of Lists

`<ol>` indicates ordered list

`<li>` indicates each item in the list.

Therefore looks somewhat like:
```html
<ol>
  <li> whatevs </li>
  <li> whatevs2 </li>
</ol>
```
`<ul>` for unordered lists. Also requiers `<li>` for each item in the list.

`<dl>` for definition lists. Requires `<dt>` for the term being defined, and `<dd>` for the definition.

Therefore looks somewhat like:
```html
<dl>
  <dt>Sashimi</dt>
  <dd>Sliced raw fish that is...</dd>
</dl>
```

```
Nested lists?

You can put a second list inside an <li> element to create a 
sub-list of nested list
```

### Summary
* There are three types of HTML lists: ordered, unordered, and definition
* Ordered lists use numbers
* Unordered lists use bullets
* Definition lists are used to define terminology
* Lists can be nested inside one another
