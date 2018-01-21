---
title:            Setting Type Online
lecture_date:     2017-02-17 00:00:00 -0500
section:          Studio
---

### Typesetting

Typesetting is a fundamental skill for any type of graphic design. Today we&rsquo;ll go over some basics for setting type online. In the next few weeks, we&rsquo;ll do a series of exercises. This is the first exercise in the series.
<br>
[Download this file and follow along](../../assets/lectures/studio/typesetting_1.zip)

### Exercise


1. Link a typeface

    <br>For google fonts:

    ```html
    <link href="https://fonts.googleapis.com/css?family=Lato" rel="stylesheet">
    ```

    ```css
    font-family: 'Lato', sans-serif;
    ```
    <br>For custom fonts:

    ```css
    @font-face {
        font-family: 'maison-neue';
        src: url('type/MaisonNeueWEB-Book.woff') format('woff2'),
             url('type/MaisonNeueWEB-Book.woff') format('woff');
        font-weight: normal;
        font-style: normal;
    }
    ```

    and

    ```css
    font-family: 'maison-neue';
    ```

1. Divide sections into paragraphs using `<p>` `</p>` in the html. Frequently, designers indent paragraphs. When you indent a paragraph, you never indent the first one.
This CSS adds a margin after each paragraph, and indents every paragraph after the first one. You should always set your margin breaks in the CSS and not using the `<br>` tag.

    ```css
    p {
      margin-bottom: 10px;
    }

    p + p {
      text-indent: 2em;
    }
    ```

1. It's not a bad idea to start with a "mobile first" approach to your body. A solid design frequently works well at both small and large sizes.
Of course you can adjust type between moniter sizes, but if you get it right the first time, there's no need. Text size of at least 16px works well at a small screen, I usually use this as a starting point and consider it the smallest a body size should be.

    ```css
    body {
      font-size: 20px;
    }
    ```
    ```css
    h1 {
      font-size: 40px;
    }
    ```
    ```css
    h2 {
      font-size: 25px;
    }
    ```
1. On the web, six different levels of hierarchy exist, even if you don't use them all. They are separated by H1 to H6. In this tutorial, we'll just focus on h1 and h2 to get a general idea. When you're designing a website that will use a CMS (such as wordpress)
to house content, it&rsquo;s a safe bet to define all of these typesizes since the user will be editing them with a WYSIWYG editor.

1. Leading works similarly to in print, however, you generally want more space on digital screens. I usually define leading with relative increments, but for simplicity we&rsquo;ll stick with numerical increments. In print, your leading is usually 2pts larger than your copy.
On screens, this type of leading is generally too tight. I would aim for at least 6px or more.

    ```css
    line-height 26px;
    ```
1. A *measure* is the term used to describe the amount of characters per line. It is important to have a comfortable measure for reading. Generally, 45 to 75 characters per line are suggested. Many consider 65 characters ideal.
Lines that are too long lose your interest, while short lines break up the copy too much. On a large screen, you need to set up a width. You do this by adding a `max-width` in the CSS.
<br><br>
Another method, introduced by Robert Bringhurst, is to multiply the type size by 30 to get the measure. Example: 10px font would be a measure of 300px.

    ```css
    max-width: 650px;
    ```

---

### Resources

- [Pro Web Type](https://prowebtype.com/)
- [Elements of Typographic Style](http://webtypography.net/)
