---
title:            Media Queries and Mobile First Design
lecture_date:     2017-02-28 00:00:00 -0500
section:          Lab
---

### Media Queries

Media query is a CSS technique introduced in CSS3 that allows you to target specific capabilities of a device.

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

Specifying a `max-width` or `max-height` in a media query is often used when you write CSS for your website viewed on desktop,
but want to display something different at a smaller, breakpoint.

### Mobile First Media Queries

Instead of defining your media queries using `max-width`, you can also take a _mobile first_ approach,
where you define your media queries using `min-width`.

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

For example, the breakpoints in [Bootstrap's](http://getbootstrap.com/css/#grid-options) default grid are defined as:

- `< 768px` (Extra small devices Phones)
- `≥ 768px` (Small devices Tablets)
- `≥ 992px` (Medium devices Desktops)
- `≥ 1200px` (Large devices Desktops)

```css
/* The body's font-size is smaller by default */
body {
  font-size: 16px;
}

/* Tablet breakpoint */
@media (min-width: 768px) {
  body {
    font-size: 22px;
  }
}

/* Desktop breakpoint */
@media (min-width: 992px) {
  body {
    font-size: 28px;
  }
}

/* Wide screen breakpoint */
@media (min-width: 1200px) {
  body {
    font-size: 36px;
  }
}
```

---

### Resources

- [Responsive Web Design - Media Queries](https://www.w3schools.com/css/css_rwd_mediaqueries.asp)
- [Mozilla: Media Queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)
- [Brad Frost: Mobile First Responsive Web Design](http://bradfrost.com/blog/web/mobile-first-responsive-web-design/)
- [Luke Wroblewski: Mobile First](http://www.lukew.com/presos/preso.asp?26)
