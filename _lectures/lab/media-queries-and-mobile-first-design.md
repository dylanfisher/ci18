---
title:            Media Queries and Mobile First Design
lecture_date:     2017-03-08 00:00:00 -0500
section:          Lab
---

### Media Queries

Media query is a CSS technique introduced in CSS3.

It uses the `@media` rule to include a block of CSS properties only if a certain condition is true.

```css
/* If the browser window is smaller than 500px, the
   background color will change to lightblue: */

@media (max-width: 500px) {
  body {
    background-color: lightblue;
  }
}
```

Media queries can be used to target vertical rules as well:

```css
/* If the browser window is shorter than 650px, the
   font-size will change to 16px: */

@media (max-height: 650px) {
  body {
    font-size: 16px;
  }
}
```

Or to target `print`, when you want to print a webpage.

```css
@media print {
  body {
    background: white;
    color: black;
  }
}
```

Using a `max-width` or `max-height` is often used when you define desktop styles but want to display something
different at a smaller, often mobile, breakpoint.

### Mobile First Media Queries

Instead of defining your media queries using `max-width`, it is often better to take a _mobile first_ approach,
where you define your queries using `min-width`.

```css
/* The body's background is set to lightblue by default,
   and when the browser's width is a minimum of 500 pixels wide,
   the background is set to white. */

body {
  background-color: lightblue;
}

@media (min-width: 500px) {
  body {
    background-color: white;
  }
}
```

A mobile first approach to media queries encourages you to define the CSS that applies to your mobile breakpoint
first. This is beneficial because the CSS at mobile is often simpler, and it is better to add additional complexity
that applies to larger breakpoints after your core mobile styles.

The points at which a media query takes affect are referred to as breakpoints. At the start of a project
you will often begin by identifying a series of breakpoints in your design and match those in your code.

The breakpoints in [Bootstrap's](http://getbootstrap.com/css/#grid-options) default grid are defined as:

- < 768px (Extra small devices Phones)
- ≥ 768px (Small devices Tablets)
- ≥ 992px (Medium devices Desktops)
- ≥ 1200px (Large devices Desktops)

### Media Queries in our own Grid System

A practical example of a mobile first media query can be applied to the grid systems we created in Week 4: [Creating Structure with HTML and CSS](/lectures/lab/creating-structure-with-html-and-css).

In our 12 column grid system we may find that at the mobile breakpoint the smaller column sizes are too small.
Instead, we want all of our columns to be 100% width at mobile, and only begin to take on their column sizes
when the window width is greater than or equal to 768px.

Assuming our columns look like `<div class="col col-6"></div>`, and our CSS looks like:

```css
.col {
  float: left;
}

.col-1  { width: 8.33%; }
.col-2  { width: 16.66%; }
.col-3  { width: 25%; }
.col-4  { width: 33.33%; }
.col-5  { width: 41.66%; }
.col-6  { width: 50%; }
.col-7  { width: 58.33%; }
.col-8  { width: 66.66%; }
.col-9  { width: 75%; }
.col-10 { width: 83.33%; }
.col-11 { width: 91.66%; }
.col-12 { width: 100%; }
```

If we wrap our column widths inside a media query that only applies at 768px, we can achieve our goal:

```css
.col {
  float: left;
}

/* Column widths are only applied when the browser's width
   is at least 768px wide */
@media (min-width: 768px) {
  .col-1  { width: 8.33%; }
  .col-2  { width: 16.66%; }
  .col-3  { width: 25%; }
  .col-4  { width: 33.33%; }
  .col-5  { width: 41.66%; }
  .col-6  { width: 50%; }
  .col-7  { width: 58.33%; }
  .col-8  { width: 66.66%; }
  .col-9  { width: 75%; }
  .col-10 { width: 83.33%; }
  .col-11 { width: 91.66%; }
  .col-12 { width: 100%; }
}
```

Since the columns are `block` level attributes, they will be 100% width by default, and only begin taking
on the width we define _inside_ the media query block.

Now let's take our grid a step further and make it so we can define different column sizes at mobile as well.
To do this we will create an additional series of CSS classes that will represent the different breakpoints
we've identified for our project.

We will use 2 breakpoints for simplicy: an `xs` (extra small) breakpoint and a `sm` (small) breakpoint. The `sm`
breakpoint will apply when the browser width is at least 768px wide, and the `xs` breakpoint will apply when the
browser width is less than 768px.

```css
/* Elements with a col-xs-* class have a width applied by default */
.col-xs-1  { width: 8.33%; }
.col-xs-2  { width: 16.66%; }
.col-xs-3  { width: 25%; }
.col-xs-4  { width: 33.33%; }
.col-xs-5  { width: 41.66%; }
.col-xs-6  { width: 50%; }
.col-xs-7  { width: 58.33%; }
.col-xs-8  { width: 66.66%; }
.col-xs-9  { width: 75%; }
.col-xs-10 { width: 83.33%; }
.col-xs-11 { width: 91.66%; }
.col-xs-12 { width: 100%; }

/* Elements with a col-sm-* class will be applied when
   the browser width is 768px or wider, and override the
   xs width. */
@media (min-width: 768px) {
  .col-sm-1  { width: 8.33%; }
  .col-sm-2  { width: 16.66%; }
  .col-sm-3  { width: 25%; }
  .col-sm-4  { width: 33.33%; }
  .col-sm-5  { width: 41.66%; }
  .col-sm-6  { width: 50%; }
  .col-sm-7  { width: 58.33%; }
  .col-sm-8  { width: 66.66%; }
  .col-sm-9  { width: 75%; }
  .col-sm-10 { width: 83.33%; }
  .col-sm-11 { width: 91.66%; }
  .col-sm-12 { width: 100%; }
}
```

With these classes defined we can create grids that have different column widths at
two different breakpoints. In practice, our HTML would look like this:

```html
<div class="container">
  <div class="row">
    <div class="col-xs-6">A column that is always 6 units wide, or 50% width</div>
    <div class="col-xs-6">Another column that is 6 units wide</div>
    <div class="col-sm-6">A column that is only 6 units wide when the browser width is at the small breakpoint</div>
    <div class="col-sm-6">Another sm-6 column</div>
  </div>
</div>
```

To see this example in action, [view this codepen](http://codepen.io/dylanfisher/pen/oZYPyz).

---

### Resources

- [Responsive Web Design - Media Queries](https://www.w3schools.com/css/css_rwd_mediaqueries.asp)
- [Mozilla: Media Queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)
- [Brad Frost: Mobile First Responsive Web Design](http://bradfrost.com/blog/web/mobile-first-responsive-web-design/)
- [Luke Wroblewski: Mobile First](http://www.lukew.com/presos/preso.asp?26)
