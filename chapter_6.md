# Chapter 6 : Tables

This chapter will teach how to:
* Use the four key elements for creating tables
* Represent complex data using tables
* Add captions to tables

### Table HTML

Each Block in the grid is referred to as a **table cell**. 

In HTML a table is written out row by row.

`<table>` element used to create a table. 

`<tr>` element indicates the start of each row. (stands for **t**able **r**ow). Closed with `</tr>` tag.

`<td>` element represent each cell of a table. (stands for **t**able **d**ata). Closed with `</td>` tag.

```
Some browsers automatically draw lines around the table and/or the individual cells.
CSS can be used to control the borders of tables.
To be explained later on
```

`<th>` element used for the same reason as `<td>`, but represents the **heading** for either a column or a row.
* stands for **t**able **h**eading
* helps people who use screen readers
* improves ability for search engines to index pages
* Gives greater appearance of tables when you start to use CSS
* can use the `scope` attribute on the `<th>` element to indicate whether it is a heading for a column or row
  * values = (`row`, `col`)
  * by default in **bold** and in the middle of the cell

Even if a cell has no content, `<td>` or `<th>` element should still be used represent the presence of an empty cell.
* Otherwise the table will not render correctly

### Spanning Columns and Rows

`colspan` attribute can be used on `<th>` or `<td>` elements, indicating how many columns the cell should run across.
* When a cell extends across more than one column, the `<td>` or `<th>` cells that would have been in the place of the wider cells are not included in the code
* Therefore the row containing colspan may seem to have lesser number of cells. (skip that particular turn of cell)

`rowspan` attribute can be used on `<th>` or `<td>` elements, indicating how many rows a cell should span down the table.
* Therefore the rows after the row containing rowspan (`<tr>`) may SEEM to have less number of cells, as already been occupied by the rowspan element.

### Long Tables

Three elements that help distinguish between
* main contents of a table
* first and alst rows of a table (which may contain different content)

`<thead>` should contain the headings of the table

`<tbody>` should contain the body of the table

`<tfoot>` should contain the footer of the table

Therefore should look somehwat like:
```html
<table>
  <thead>
    <tr>
      <th>...</th>
    </tr>
  </thead>
  <tbody>
    ...similar (but <td>)
  </tbody>
  <tfoot>
    ...similar (but <td>)
  </tfoot>
</table>
```

```html
Why use these long tables (by splitting into three parts?)
- If the table is taller than screen, the browser can keep the header and footer visible
  while the contents of the table scroll
  > Thus easier to see which column the data is in
```

### OLD CODE
Old attributes which were used before HTML5 but are now done by CSS:
* width (value in pixels)
  * How wide the **table** should be
  * How wide **individual cells** should be
* cellpadding (value in pixels)
  * Add space *inside* each cell of the table 
* cellspacing (value in pixels)
  * Add space *between* each cell of the table
* border (value in pixels)
  * on both `<table>` and `<td>` to indicate width of the border
* bgcolor
  * either on entire table or individual cells
  * Value in hexcode (ex "#cccccc")

### Summary
* The `<table>` element is used to add tables to a web page
* A table is drawn out row by row. Each row is created with the `<tr>` element.
* Inside each row there are a number of cells represented by the `<td>` element (or `<th>` if it is a header)
* You can make cells of a table span more than one row or column using the **rowspan** and **colspan** attributes
* For long tables you can split the table into a `<thead>`, `<tbody>` and `<tfoot>`.
