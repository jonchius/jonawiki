---
description: getting that first webpage in
---

# ⚙️ HTML setup

Let us begin with the creation of a basic HTML file!

### Prerequisites

To create an HTML file, we could use a simple **text editor,** like [TextEdit](https://en.wikipedia.org/wiki/TextEdit) or [Notepad](https://en.wikipedia.org/wiki/Microsoft_Notepad)...

...but a **code editor, like** [Sublime](https://www.sublimetext.org) or [Visual Studio Code](https://code.visualstudio.com), helps a lot!

### The minimal HTML file

If we open the text editor, we can copy and paste the below:

```markup
<!DOCTYPE html>
<html lang="en">

    <head>
        <title>(The title that will show in the browser tab)</title>        
    </head>
    
    <body>
        <p>(The content)</p>
    </body>
    
</html>
```

* The first line tells the browser to expect an HTML document
* The actual HTML begins inside the `<html>` tag which contains an optional `lang` attribute to indicate what human language the page uses
  * the HTML continues with the `<head>` tag&#x20;
    * the `<title>` tag displays the page's name on the browser tab
  * then the `<body>` tag contains the actual content that the browser displays
    * the `<p>` tag represent a paragraph

### Closing tags

* Most HTML tags come paired with a **closing tag**
  * In the above example, we have `</title>`, `</head>`, `</p>, </body>` and `</html>`
  * Tags close in a nested hierarchy such that we _cannot_ have an outer tag close before an inner tag closes, e.g. `<body><h1></body></h1>` must instead be `<body><h1></h1></body>`

That makes up nearly the barest-bones HTML page and after that, the possibilities become endless:

```markup
<!DOCTYPE html>
<html lang="en">

    <head>
        <meta charset="utf-8" />
        <title>Page's title</title>        
    </head>
    
    <body>
        <h1>Heading 1</h1>
        <p>This forms a pararaph of some sorts. </p>
    </body>
    
</html>
```

Looking at the new tags, we have:&#x20;

* `<meta>` which provides background information about the page
  * in this case, the tag contains an attribute `charset` that tells us the page uses Unicode (a "character set" that includes the alphabets and scripts of every human language)&#x20;
* `<h1>` represents a top-level heading and, as we can guess, \<h2> would mean a second-level heading, and so on!

### Self-closing tags

* As above, we introduced `<meta charset="utf-8" />` which features a tag without a closing tag that self-closes (we can also call this a **self-closing tag**)
  * Other tags that have this feature include
    * `<link href="..." />` for stylesheets (located usually only in the `<head>` tag)
    * `<img src="..." />` for images
    * `<br />`for line breaks (like pressing "shift+return" or "shift+enter" on a word processor)
  * Note that it has become _optional_ to include the **self-closing slash**
    * e.g. it is OK to write just `<br>` but writing `<br />` will prepare us later for [JSX](../react/react-jsx.md) in [React](../react/)!
