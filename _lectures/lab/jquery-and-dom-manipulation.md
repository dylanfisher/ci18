---
title:            jQuery and DOM Manipulation
subtitle:         An introduction to the jQuery JavaScript library and how to use it to manipulate the DOM
lecture_date:     2017-04-05 00:00:00 -0500
section:          Lab
---

### What is jQuery?

jQuery is a fast, small, and feature-rich JavaScript library. It makes things like HTML document traversal and manipulation, event handling, animation, and Ajax much simpler with an easy-to-use API that works across a multitude of browsers. With a combination of versatility and extensibility, jQuery has changed the way that millions of people write JavaScript.

- [jquery.com](https://jquery.com/)

jQuery is a _JavaScript Library_, meaning it is a library of pre-written JavaScript which allows for easier development of JavaScript-based applications.
jQuery is still just JavaScript, but it creates a new series of functions that you can use in addition to vanilla JavaScript.

### What is the DOM?

DOM stands for Document Object Model. When a web page is loaded, the browser creates a Document Object Model of the page. This is what you
see on the webpage when you view it in your browser.

You can use JavaScript to manipulate the DOM, and jQuery makes it easy to do this.

- [Read more](https://www.w3schools.com/js/js_htmldom.asp)

### Incuding jQuery in your project

To include jQuery in your project, go to [https://jquery.com/](https://jquery.com/) and click the download button. Then, download the
"compressed, production jQuery" package of the latest version. Right now that's version 3.2.0 [click here for direct download](https://code.jquery.com/jquery-3.2.0.min.js).

Move the jQuery script you download into your project's javascripts folder, and link to it right before including your other JavaScript files.

```html
<!DOCTYPE html>
<html>
<head>
  <title>jQuery Test</title>
  <link rel="stylesheet" href="css/style.css">
  <script src="/js/jquery-3.2.0.min.js"></script>
  <script src="/js/main.js"></script>
</head>
<body>
  <!-- Your HTML code here -->
</body>
</html>
```

In this example we include the jQuery library right before the `main.js` file. This is important because you must include JavaScript libraries before
writing any code that references code in those libraries.

### Using jQuery

When you write JavaScript using jQuery, you should always wrap the JavaScript in a special jQuery function that waits to run the code until the
rest of the document (DOM) has finished loading.

```js
$(function() {
  // Your JavaScript goes inside this special function wrapper.
});
```

Don't worry too much about why this is necessary for now, just remember to always write your jQuery code inside the `$(function() { ... });` function wrapper.

### Syntax

The basic jQuery syntax is `$(selector).action()`.

- A `$` sign to define/access jQuery
- A `(selector)` to "query (or find)" HTML elements
- A jQuery `action()` to be performed on the element(s)

Examples

`$(this).hide()` - hides the current element.

`$("p").hide()` - hides all `<p>` elements.

`$(".test").hide()` - hides all elements with `class="test"`.

`$("#test").hide()` - hides the element with `id="test"`.

```js
$(function() {
  // Select CSS classes
});
```

[Read more](https://www.w3schools.com/jquery/jquery_syntax.asp)

### Interactive examples

```js
$(function() {
  $('.jquery-dom-css-test').click(function() {
    if ( $('html').hasClass('active') ) {
      $('html').removeClass('active').css('background', '');
    } else {
      $('html').addClass('active').css('background', '#67DAA6');
    }
  });
});
```
<script>
  $(function() {
    $('.jquery-dom-css-test').click(function() {
      if ( $('html').hasClass('active') ) {
        $('html').removeClass('active').css('background', '');
      } else {
        $('html').addClass('active').css('background', '#67DAA6');
      }
    });
  });
</script>

<button class="jquery-dom-css-test">Change the background color</button>

```js
$(function() {
  $('.jquery-dom-remove-footer').click(function() {
    $('.sidebar .footer').remove();
  });
});
```

<script>
  $(function() {
    $('.jquery-dom-remove-footer').click(function() {
      $('.sidebar .footer').remove();
    });
  });
</script>

<button class="jquery-dom-remove-footer">Remove the sidebar footer</button>

```js
$(function() {
  $('.jquery-dom-add-some-text').click(function() {
    $(this).after("Here's some text that was just added dynamically! Wow! ");
  });
});
```

<script>
  $(function() {
    $('.jquery-dom-add-some-text').click(function() {
      $(this).after("Here's some text that was just added dynamically! Wow! ");
    });
  });
</script>

<button class="jquery-dom-add-some-text">Add some text after this button</button>
