---
description: allowing the user to enter alphanumeric content
---

# 🔤 HTML input: text

### Essentials

At the minimal, the `<input>` field for `type="text"` looks like this:

```markup
<form action="destination.html" method="post">

    <label for="fname">First name</label>
    <input type="text" name="fname">

    ...    
    
</form>
```

Other attributes can include:&#x20;

* `maxlength` (enforces a maximum character length of input)
* `minlength` (enforces a minimum character length of input)
* `required` (enforces some kind of value; cannot stay blank)
* `id` (identifies the field uniquely)
  * differs from `name` in that `name` does not enforce uniqueness

```html
<form action="destination.html" method="post">

    <label for="fname">First name</label>
    <input type="text" name="fname" id="fname" maxlength="50" required>

    ...    
    
</form>
```

### Takeaways

Most of those attributes are self-explanatory and "google-able" but taking note that:

* the difference between a `name` and `id` lies on the uniqueness requirement of `id`
* we can use `name` multiple times in the same HTML document!
