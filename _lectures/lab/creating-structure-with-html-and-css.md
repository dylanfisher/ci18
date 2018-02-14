---
title:            Creating Structure with HTML and CSS
lecture_date:     2017-02-14 00:00:00 -0500
section:          Lab
---

### Creating structure with CSS Flexbox

[Download the flexbox layout starter kit](/assets/lectures/lab/creating-structure-from-html-and-css/flexbox-tutorial.zip)

The Flexible Box Module, usually referred to as flexbox, was designed as a one-dimensional layout model, and as a method that could offer space distribution between items in an interface and powerful alignment capabilities. This article gives an outline of the main features of flexbox, which we will be exploring in more detail in the rest of these guides. [\[developer.mozilla.org\]](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)

![Flex direction terms](/assets/lectures/lab/creating-structure-from-html-and-css/flex-direction-terms.svg)

### Basic structure

Layouts made using flexbox will typically consist of a container element (the flex container) and a series of items inside the container (the flexible elements).

```html
<div class="flex-container">
  <div class="flex-item">
    <p>Lorem ipsum dolor sit amet.</p>
  </div>
  <div class="flex-item">
    <p>Another flexible item</p>
  </div>
</div>
```

```css
.flex-container {
  display: flex;
}
```

Review the starter kit examples for ideas about how you can structure your HTML and CSS
in a way that makes it easy to create layouts using flexbox.

See if you can apply these techniques to your current Click, Click projects.

---

### Other resources

- [philipwalton.github.io/solved-by-flexbox](https://philipwalton.github.io/solved-by-flexbox/)
- [an-animated-guide-to-flexbox](https://medium.freecodecamp.org/an-animated-guide-to-flexbox-d280cf6afc35)
- [css-tricks.com/snippets/css/a-guide-to-flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [flexboxfroggy.com](http://flexboxfroggy.com/)
