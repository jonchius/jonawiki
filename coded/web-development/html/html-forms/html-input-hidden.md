---
description: allowing a programmer to include hidden information upon form submission
---

# ⛔ HTML input: hidden

### Essentials

In a form, an `<input>` tag with a `type="hidden"` would usually not appear on the form interface but remain in the background:

```markup
<form action="destination.html" method="post">
  
  <input type="hidden" name="cantsee" value="this">
  
  <div>
    <label for="fname">First name</label>
    <input type="text" name="fname" id="fname">
  </div>
  
  ...

  <div>
    <input type="reset">
    <input type="submit" value="Go!"> 
  </div>
  
</form>
```

### Takeaways

* When the form submits, it will send the `hidden` field with `cantsee` as the key and `this` as the value
