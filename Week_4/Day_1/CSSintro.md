## CSS Fundamentals

CSS is language that specifies a page's appearance.
CSS code is made of "static" rules. Each rule takes one or more selectors and gives specific values to a number of visual properties. Those properties are then applied tot he page elements indicated by the selectors.

Methods of implementing CSS into HTML:
```html
<!-- You need to include the css file in your page's <head>. This is the
     recommended method. Refer to http://stackoverflow.com/questions/8284365 -->
<link rel='stylesheet' type='text/css' href='path/to/style.css'>

<!-- You can also include some CSS inline in your markup. -->
<style>
   a { color: purple; }
</style>

<!-- Or directly set CSS properties on the element. -->
<div style="border: 1px solid red;">
</div>
```

Specificity is an algorithm used by browsers to determine the CSS declaration that is the most relevant to an element. It then determines the property value to apply to the element. 
The order for specificity goes:
1. Inline Styles
2. IDs
3. Classes, attributes, and pseudo-classes
4. Elements and pseudo-elements