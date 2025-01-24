---
description: defining the objects of an web page
---

# 🏷️ HTML tag structure

HTML tags follow a basic structure of **definition**, **attributes** and **content:**

* Definition, as the tag/object itself, e.g. `<h1>` for a heading
* Attributes, describe the tag, e.g. `src` for the source of an `<img>` tag
  * `<img src="file.jpg" />`
* Content, which houses additional objects and information
  * these may include plain text or _other "child" tags_

### Content inside HTML tags

If we were to include content inside an HTML tag, the tag would need an opening and closing component, for example:

```xml
<h1>(content)</h1>
```

As in the first-level heading above

* `<h1>` makes up the opening tag
* `</h1>` makes up the closing tag

### Nesting

We could even include tags inside tags! Of course, we always do this with the `<html>` tag:

```xml
<html>
    <body>
        <h1>Heading</h1>
    </body>
</html>
```

When we nest a tag, we must close the innermost tag before closing the outer tag (in the above example, we must close `h1` before closing `body` , which we, in turn, close before `html`)

