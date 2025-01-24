---
description: listing the most frequently used building blocks of a webpage
---

# 🏷️ Common HTML tags

### Headings : \<h1> to \<h6>

`<h1>` ... `<h6>`

* Headings have a hierarchy from 1 (the top) to 6 (the bottom)
  * `<h1>...</h1>` will lead while `<h2>...</h2>` may or may not follow an `<h1>`
  * All full-sized HTML pages should have an `<h1>...</h1>`
  * As an aside, documents (think legal documents) rarely have a proper `<h5>` and `<h6>` because by the point, the document will have become too difficult to follow&#x20;
    * try to not have anything further below the `<h4>` level for simple HTML pages

{% hint style="danger" %}
Do _not_ use these headings as font sizes, as the numbers serve a structural purpose of making "levels" for the document; we will adjust font sizes later with [CSS](../../css/)
{% endhint %}

### Paragraphs : \<p>

`<p>`

* Exactly as advertised: paragraphs of text
* By default, paragraphs will have dividing spaces between them like in written text

### Lists : \<ul>, \<ol>, \<li>

`<ul>` (unordered list) `<ol>`(ordered list) `<li>` (list item)

* An unordered list looks like a list of bullets (like this one!)
* An ordered list has numbers (or numerals)
* There exist many ways to style the bullets of these lists (more on this later)
* A list item appears inside of an unordered or ordered list

### Importance : \<strong>

`<strong>`

* Usually shows the text in **bold** type
* Conveys the idea of an **important keyword** in the text of a document

### Emphasis : \<em>

`<em>`

* Usually shows the text in _italic_ type
* Conveys the idea of _stress_ on a word or phrase

### Strikeout : \<del>, \<strikeout>

`<del>` or `<strikeout>`

* Usually shows the text ~~slashed~~ horizontally ~~like this~~
* Conveys the idea of removal of a text while still making the text visible

### Quotations : \<blockquote>

`<blockquote>`

* Usually shows the text indented
* Conveys the idea that the text is a reference of some other text

```markup
<html>

    <head>
    
        <title>Page title</title>
        
    </head>
    
    <body>
    
        <h1>Heading 1</h1>
        
        <p>Some <strong>text</strong> to <em>welcome you</em>!</p>
        
        <h2>A list</h2>
        
        <ul>
        
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            
        </ul>
        
        <blockquote>We have a dream!</blockquote>
        
        <p>This page has <del>no</del> content!</p> 
        
    </body>

</html>
```

### Links : \<a>

`<a href="https://website.com">Website.com</a>`

The `a` means "anchor" and signifies that it points to another page or site altogether:

* The `href` means "hypertext reference" (we only need to know it means "address")
* We will see in [HTML tag attributes](html-tag-attributes.md) that href is an **attribute**

### Images : \<img>

`<img src="/brand-x-logo.jpg" alt="logo of Brand X" />`

Just like the tag for a link, the img tag intuitively has a couple of attributes:

* The `src` means "source"
* We will also see more of this later in [HTML tag attributes](html-tag-attributes.md)

### Other common tags

We will also have a look at other high-frequency tags that will require pages of their own, namely:

* [\<div>](../html-div.md) (along with its variants)
* [\<table>](../html-table-tags.md)
* [\<form>](../html-forms/) (and \<input>)
* [\<head>](../html-head.md) (and \<meta> as well as \<title>)
