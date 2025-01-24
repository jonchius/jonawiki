---
description: organizing similar records of data together on a webpage
---

# 🍽️ HTML \<table> tags

**Tables** display groups of similar data as a grid-like structure:

* Rows typically show data observations of individual phenomena
* Table typically show values that describe those individuals

For example:

* A row could show a city
* Each column could show data that describes a single city, e.g.
  * country
  * population
  * mayor

{% hint style="info" %}
To use a linguistics analogy, we could say that rows form the "nouns" and that columns form the "adjectives" of tables!
{% endhint %}

### Structure

As part of semantic HTML, `<table>` tags allow us to make "two-dimensional lists" with headers, rows, columns and footers:

```markup
<table>
    <caption>Explaining the table for accessibility</caption>
    <thead>
        <tr>
            <th scope="col">Column 1 Header</th>
            <th scope="col">Column 2 Header</th>
            <th scope="col">Column 3 Header</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Row 1, Column 1</td>
            <td>Row 1, Column 2</td>
            <td>Row 1, Column 3</td>
        </tr>
        <tr>
            <td>Row 2, Column 1</td>
            <td>Row 2, Column 2</td>
            <td>Row 2, Column 3</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>Total, Column 1</td>
            <td>Total, Column 2</td>
            <td>Total, Column 3</td>
        </tr>
    </tfoot>
</table>    
```

### Elements

We will look at the tags above in the table below:

<table><thead><tr><th width="188">Tag</th><th width="127.33333333333331">Nesting level</th><th>Meaning</th></tr></thead><tbody><tr><td>&#x3C;table></td><td>0</td><td>the table</td></tr><tr><td>&#x3C;caption></td><td>1</td><td>a write-up explaining the table (usually used for screen readers for accessibility and hidden from sighted users)</td></tr><tr><td>&#x3C;thead></td><td>1</td><td>table heading section (usually a row to describe each column)</td></tr><tr><td>&#x3C;tr></td><td>2</td><td>table row</td></tr><tr><td>&#x3C;th></td><td>3</td><td>table heading</td></tr><tr><td>&#x3C;tbody></td><td>1</td><td>table body (main content)</td></tr><tr><td>&#x3C;td></td><td>3</td><td>table definition (data cell)</td></tr><tr><td>&#x3C;tfoot></td><td>1</td><td>table footer (usually a row for numerical totals)</td></tr></tbody></table>

### Attributes

One attribute to note is `scope` for table headings; these simply denote whether the heading refers to:

* items that appear vertically below that heading as a column (`col`)
* items that follow that heading as a row (`row`)&#x20;

Older attributes used to live in the `<table>` tag (e.g. `cellspacing` and `cellpadding`) but CSS takes care of them of these days!

{% hint style="warning" %}
Web developers formerly used the `<table>` tag for layout purposes to divide up sections of a page

However, this practice has become highly frowned upon and we prefer to use the `<div>` tag today!
{% endhint %}
