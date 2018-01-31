---
title:            HTML & CSS, Part 1
subtitle:         An introduction to semantic markup, and Cascading Style Sheets
lecture_date:     2017-02-01 00:00:00 -0500
section:          Lab
---

### HTML Basics

1. All HTML documents must start with a document type declaration: `<!DOCTYPE html>`
2. The HTML document itself begins with `<html>` and ends with `</html>`
3. The visible part of the HTML document is between `<body>` and `</body>`

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My HTML Document</title>
  </head>
  <body>
    <p>A very basic HTML page</p>
  </body>
</html>
```

### Common HTML Tags

[View this example on CodePen](http://codepen.io/dylanfisher/pen/rjpPxb/)

```html
<h1>This is heading 1</h1>
<h2>This is heading 2</h2>
<h3>This is heading 3</h3>
<h4>This is heading 4</h4>
<h5>This is heading 5</h5>
<h6>This is heading 6</h6>

<p>This is a paragraph</p>

To break<br>lines<br>in a<br>paragraph,<br>use the br element.

<hr>
The hr tag creates a horizontal line in an HTML page.

<em>This is emphasized text</em>

<strong>This is strong text</strong>

<!--This is a comment. Comments are not displayed in the browser-->

<ol>
  <li>This is an</li>
  <li>Ordered</li>
  <li>List</li>
</ol>

<ul>
  <li>This is an</li>
  <li>Unordered</li>
  <li>List</li>
</ul>

The <code>code element</code> example

The <em>em element</em> example

The <mark>mark element</mark> example

The <small>small element</small> example

The <strong>strong element</strong> example

The <sub>sub element</sub> example

The <sup>sup element</sup> example

<input type="radio" name="rad"> Radio input

<input type="checkbox"> Checkbox input

Text input <input type="text" value="default value that goes on and on without stopping or punctuation">

<a href="http://www.newschool.edu">This is a link</a>

This is an image <img src="/assets/favicon.png" alt="Eye favicon">
```

An HTML element usually consists of a start tag and end tag, with the content inserted in between:

```html
<tagname>Content goes here...</tagname>
```

The HTML element is everything from the start tag to the end tag:

```html
<p>My first paragraph.</p>
```

---

### HTML, CSS, Javascript

Three technologies form the cornerstone of every page you view in a web browser. These are HTML, CSS and Javascript.
Each technology, at it's core, serves a single purpose.

| HTML | CSS | Javascript |
| --- |---| ---|
| Content | Style | Behavior |
| _What it says_ | _What it looks like_ | _What it does_ |

---

### Markup Language: the structure of your text

"A markup language is a system for annotating a document in a way that is syntactically distinguishable from the text."

HTML is _not_ a programming language; it is a a markup language that provides the means to create content and structure
from text. These documents are created from a series of semantics blocks (HTML tags). When crafting HTML pages, always
keep in mind the semantics of the tag to best reflect the intent of the text. For example, a list of items makes
more sense as an unordered list of list items `<ul><li>` than as a series of paragraph tags `<p>`.

### HTML is content, not style

The HTML you write describes the text in your document, it does not style it. You should avoid inline styles that
couple the aeshetic presentation of your document with the markup structure. Instead, use an external stylesheet
to add styles to your structure.

---

### Chrome DevTools: Viewing HTML in the browser

[Chrome DevTools](https://developer.chrome.com/devtools)

### Accessing the DevTools

1. Select the Chrome menu Chrome Menu at the top-right of your browser window, then select Tools > Developer Tools.
1. Right-click on any page element and select Inspect Element.

DevTools is a powerful tool that enables you to view, alter and monitor the HTML, CSS and Javascript that are displayed
in your browser. While developing for the web, it is important that you _always_ have DevTools open to help speed up the
development process and identity code errors.

When you inspect a page, you are viewing the contents of the page in an identical state to what's displayed in your browser.
This is different that when you view the source code of the page, which you can do by selecting View > Developer > View Source.

---

### CSS: Adding an external stylesheet

CSS stands for Cascading Style Sheets. CSS is used to give style and change the appearance of your structured HTML.

CSS can be added to HTML in 3 ways:

1. Inline - by using the style attribute in HTML elements
1. Internal - by using a `<style>` element in the `<head>` section
1. External - by using an external CSS file

It is a best practice to store your styles in an external stylesheet, linked to from your HTML document's head. For
the purpose of this class, all your styles will be stored using the external method.

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="style.css">
  </head>
<body>
  <p>My structure</p>
</body>
</html>
```

This is what style.css looks like:

```css
body {
  background-color: white;
}

h1 {
  color: blue;
}

p {
  color: red;
}
```

### Structure of a CSS selector

<div class="css-selector-image-example">
  <img src="/assets/lectures/lab/html-css-part-1/css_selector.gif" alt="CSS Selector Example">
</div>

### Targeting elements with CSS

Individual HTML elements can be targeted directly with css, as in the example above. For example, the `body` element
is targeted directly, and all `p` elements are targeted with the `p` tag. You will often want to target only certain
elements on a page. The best way to do this is what _classes_ added to your HTML elements.

HTML elements can have many attributes added in between the first tag name. One of these attributes is `class`. A class
gives you a way to select the element with CSS and Javascript.

```html
<tagname class="my-class another-class test"></tagname>
```

```html
<p>Not so special. Mostly gray and sad.</p>
<p class="special-paragraph">This paragraph is special, that's why it's pink.</p>
<p>Also not so special.</p>
```

```css
p {
  color: gray;
}

.special-paragraph {
  color: pink;
}
```

In the above CSS, the paragraph with the special-paragraph class becomes pink, eventhough we colored all paragraph tags
gray in the line before. This is because of two reasons. First, CSS _cascades_. That is, styles that are defined later take precedence over the styles
that are defined before. Second, CSS properties have different levels of specificity. Type selectors (like the `<p>` tag) are
least specific. Class selectors are more specific, and ID selectors are most specific.

For now, just remember that it's best practice to be less specific in your CSS. That means, only use type selectors or
class selectors to style your HTML. Don't use ID's to style HTML.

```html
<p>Not so special. Mostly gray and sad.</p>
<p id="most-special-paragraph" class="special-paragraph">This paragraph is special, that's why it's pink.</p>
<p>Also not so special.</p>
```

```css
p {
  color: gray;
}

#most-special-paragraph {
  color: red;
}

.special-paragraph {
  color: pink;
}
```

In this example, eventhough we define the special-paragraph style lower in the CSS cascade, the most-special-paragraph
ID selector is so specific it overrides the pink color, and the paragraph becomes red. Additionally, there can be many
attributes with the same class on a page, but there can only ever be one element with the same ID on a page.

If you _really_ wanted the special-paragraph to be pink, you can use a special `!important` rule to force this attribute's
specificity to the maximum, which will override all other rules, except for `!important` rules that come after (cascade) after this one.

```css
p {
  color: gray;
}

#most-special-paragraph {
  color: red;
}

.special-paragraph {
  color: pink !important;
}
```

Please note, however, that using `!important` is _not_ good practice and should be avoided at all costs unless you
fully understand why you are using it. It's better to be as unspecific as possible, and apply specificity only as
necessary.

### CSS Properties

You can control how an element looks using a large number of different CSS properties. Some common ones include:

- color
- background
- border
- outline
- margin
- padding
- width/height
- text
- fonts
- position
- display
- float

These properties can be mixed and matched in any combination when styling an element. For example, to make our special-paragraph
even more special, we can apply many CSS properties to it using this syntax:

```css
.special-paragraph {
  color: pink;
  background: black;
  border: 1px solid blue;
  margin: 10px;
  padding: 5px;
  font-family: monospace;
  font-size: 24px;
}
```

Each property has a unique set of values that you may use to add style. For example, the `color` property accepts a
valid color format, such as the web safe color word `pink`. You can also pass color as a hexcode, such as `#ffc0cb`, or
any other valid css color format.

However, the values that are available to the `margin` property are different than those of the `color` property. It wouldn't
make sense to pass the color pink to a margin. Each CSS property is unique, and it's important to become familiar with the
values that are available to each property.

---

### Box Model

All HTML elements can be considered as boxes. In CSS, the term "box model" is used when talking about design and layout.

The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content. The image below illustrates the box model:

![Box Model](/assets/lectures/lab/html-css-part-1/box-model.svg)

- Content - The content of the box, where text and images appear
- Padding - Clears an area around the content. The padding is transparent
- Border - A border that goes around the padding and content
- Margin - Clears an area outside the border. The margin is transparent

The box model allows us to add a border around elements, and to define space between elements.

<div class="box-model-example">
  <span class="box-model-example__content-text">Box One</span>
</div>

<div class="box-model-example">
  <span class="box-model-example__content-text">Box Two</span>
</div>

---

### Positioning Elements in CSS

Positioning in CSS is done is usually done with one of four attributes:

- Static
- Relative
- Absolute
- Fixed

```css
position: static;
```

HTML elements are positioned static by default.

Static positioned elements are not affected by the top, bottom, left, and right properties.

An element with `position: static;` is not positioned in any special way; it is always positioned according to the normal flow of the page.

```css
position: relative;
```

An element with `position: relative;` is positioned relative to its normal position.

Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.

```css
position: fixed;
```

An element with `position: fixed;` is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The top, right, bottom, and left properties are used to position the element.

A fixed element does not leave a gap in the page where it would normally have been located.

```css
position: absolute;
```

An element with `position: absolute;` is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).

However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.

[Read](http://www.w3schools.com/css/css_positioning.asp)
[more](https://developer.mozilla.org/en-US/docs/Web/CSS/position)
[about](http://alistapart.com/article/css-positioning-101)
[CSS](https://css-tricks.com/almanac/properties/p/position/)
[positioning](http://blog.teamtreehouse.com/css-positioning).

