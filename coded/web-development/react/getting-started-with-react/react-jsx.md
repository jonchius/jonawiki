---
description: React's HTML-like markup language
---

# ⚛️ React JSX

[Earlier](./), we had a brief look at **JSX** (JavaScript XML) and so we will now have a closer look at:

* React without and with JSX
* JSX tag naming conventions
* JSX attribute naming conventions&#x20;
* mandatory self-closing tags
* containing JSX with a single div or fragment

Such features make JSX a little different from HTML, while it gives us a more familiar way to build user interfaces with React:

### React without JSX

Without JSX, we would have to type in lengthy and bracket-heavy JavaScript method calls like such:

```javascript
const createSpan = () => {
    return React.createElement("span", { className: 'someclass' }, "in-line text")
}
```

...just to output an HTML tag like this:&#x20;

```html
<span className="someclass">in-line text</span>
```

In general:

```
const createComponent = () => {
    return React.createElement("SomeComponentTagName", { className
```

* the first argument contains the component (element's) name
* the second argument contains the component's attribute
* finally, zero or more arguments at the end contain the component's children (we'll see what this means at the end of this page)

### React with JSX

With JSX, the cryptic JavaScript `createElement` call becomes more similar to HTML:

```jsx
const createSpan = () => {
    return (
        <span className="someclass">in-line text</span>
    )
}
```

#### JSX tag naming conventions

Unlike HTML tags, JSX tags can have almost any name with the following conventions:

* first letter capitalized
* single "worded" and camel-cased as such: "CamelCase"&#x20;

#### JSX attribute naming conventions

As with tags, JSX allows a greater range of names for attributes with the following conventions:

* first letter lowercase
* single "worded" and camel-cased as such: "camelCase"

As an example:

```jsx
const createSpan = () => {
    return (
        <span className="someclass" dataSet="myDataset">in-line text</span>
    )
}
```

Restrictions with certain words also do occur (due to JavaScript reserved keywords) so use:

* `className` instead of `class`
* `htmlFor` instead of `for`

#### Self-closing tags

Unlike HTML tags, all JSX tags must self-close, i.e. have either a closing tag, or a closing slash before the closing bracket of a JSX tag:

<pre class="language-jsx"><code class="lang-jsx"><strong>return (
</strong><strong>    &#x3C;Card> ... &#x3C;/Card>
</strong>    &#x3C;Image src="file.jpg" />
)
</code></pre>

#### Encapsulation by a single tag

All JSX tags must have a "container" tag that encapsulates, or wraps around, JSX tags:

```jsx
return (
    <Container>
        <Card> ... </Card>
        <Image src="file.jpg" />
    </Container>
)
```

A newer kind of container tag is known as a "Fragment" and looks something like a tag with the name removed:

```jsx
return (
    <>
        <Card> ... </Card>
        <AnotherSiblingComponent dataSet="mydataset"/>
        <Image src="file.jpg" />
    </>
)
```

That looks like a mistake but it's not! It simply allows the developer not to come up with a new name for a container tag :relaxed:

### React without JSX - again!

As alluded from the above, we also call each child tag, a "**child element**" or, more commonly, a "**child component**".

Now, if we were to write the last snippet without JSX, it would look like this:

```javascript
return React.createElement(
    "div",
    null,
    React.createElement("Card", null, "..."),
    React.createElement("AnotherSiblingComponent", { dataSet: "mydataset" }), 
    React.createElement("Image", { src: "file.jpg" })
)   
```

"Vanilla React" indeed looks a lot more error-prone than JSX...
