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

### Summary
* The `<table>` element is used to add tables to a web page
* A table is drawn out row by row. Each row is created with the `<tr>` element.
* Inside each row there are a number of cells represented by the `<td>` element (or `<th>` if it is a header)
* You can make cells of a table span more than one row or column using the **rowspan** and **colspan** attributes
* For long tables you can split the table into a `<thead>`, `<tbody>` and `<tfoot>`.
