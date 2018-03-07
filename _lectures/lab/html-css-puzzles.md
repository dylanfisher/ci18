---
title:            HTML/CSS Puzzles
lecture_date:     2017-02-28 00:00:00 -0500
section:          Lab
hidden:           true
---

### Results

<table style="margin: 0 0 5px;">
  {% assign github_username = 'funge549.github.io' %}
  {% assign url_base = '/html-css-puzzles/puzzle-' %}
  <td style="width: 50%; padding: 10px;">{{ github_username }}</td>
  <td style="width: 50%; padding: 10px;">{% for num in (1..6) %}<a href="http://{{ github_username }}{{ url_base }}{{ forloop.index }}">{{ forloop.index }}</a>{% unless forloop.index == 6 %}, {% endunless %}{% endfor %}</td>
</table>

<table style="margin: 0 0 5px;">
  {% assign github_username = 'esragumrukculer.github.io' %}
  {% assign url_base = '/html-css-puzzles/puzzle-' %}
  <td style="width: 50%; padding: 10px;">{{ github_username }}</td>
  <td style="width: 50%; padding: 10px;">{% for num in (1..6) %}<a href="http://{{ github_username }}{{ url_base }}{{ forloop.index }}">{{ forloop.index }}</a>{% unless forloop.index == 6 %}, {% endunless %}{% endfor %}</td>
</table>

<table style="margin: 0 0 5px;">
  {% assign github_username = 'kims889.github.io' %}
  {% assign url_base = '/html-css-puzzles/puzzle-' %}
  <td style="width: 50%; padding: 10px;">{{ github_username }}</td>
  <td style="width: 50%; padding: 10px;">{% for num in (1..6) %}<a href="http://{{ github_username }}{{ url_base }}{{ forloop.index }}">{{ forloop.index }}</a>{% unless forloop.index == 6 %}, {% endunless %}{% endfor %}</td>
</table>

<table style="margin: 0 0 5px;">
  {% assign github_username = 'seowxx.github.io' %}
  {% assign url_base = '/7_html-css-puzzles/puzzle-' %}
  <td style="width: 50%; padding: 10px;">{{ github_username }}</td>
  <td style="width: 50%; padding: 10px;">{% for num in (1..6) %}<a href="http://{{ github_username }}{{ url_base }}{{ forloop.index }}">{{ forloop.index }}</a>{% unless forloop.index == 6 %}, {% endunless %}{% endfor %}</td>
</table>

<table style="margin: 0 0 5px;">
  {% assign github_username = 'lie771.github.io' %}
  {% assign url_base = '/html-css-puzzles/puzzle-' %}
  <td style="width: 50%; padding: 10px;">{{ github_username }}</td>
  <td style="width: 50%; padding: 10px;">{% for num in (1..6) %}<a href="http://{{ github_username }}{{ url_base }}{{ forloop.index }}">{{ forloop.index }}</a>{% unless forloop.index == 6 %}, {% endunless %}{% endfor %}</td>
</table>

<table style="margin: 0 0 5px;">
  {% assign github_username = 'walde906.github.io' %}
  {% assign url_base = '/html-css-puzzles/puzzle-' %}
  <td style="width: 50%; padding: 10px;">{{ github_username }}</td>
  <td style="width: 50%; padding: 10px;">{% for num in (1..6) %}<a href="http://{{ github_username }}{{ url_base }}{{ forloop.index }}">{{ forloop.index }}</a>{% unless forloop.index == 6 %}, {% endunless %}{% endfor %}</td>
</table>

---

### Instructions

1. Download the [starter kit](/assets/lectures/lab/html-css-puzzles/html-css-puzzles.zip).
1. Try to complete each task using as short and simple code as possible. Try to match your CSS and
HTML as close as possible to the image. This includes the color, font size, width/height, etc.
  - You may find the _Digital Color Meter_ on your Mac computer helpful for copying colors.
1. Each task should reflect how the reference image looks at both the mobile and desktop breakpoints. The reference images
are a 1:1 scale when viewed at 100% width. Make sure you click each image to open it in a new tab and view it at 100% width so that you get the scale correct.
Each desktop screenshot is 1000px wide, and each mobile screenshot is 400px wide.

---

### 1. Inline Block

<a href="/assets/lectures/lab/html-css-puzzles/1-desk.jpg" target="_blank">
  <img src="/assets/lectures/lab/html-css-puzzles/1-desk.jpg">
</a>

<a href="/assets/lectures/lab/html-css-puzzles/1-mobile.jpg" target="_blank">
  <img src="/assets/lectures/lab/html-css-puzzles/1-mobile.jpg">
</a>

---

### 2. Quotes in Cards

<a href="/assets/lectures/lab/html-css-puzzles/2-desk.jpg" target="_blank">
  <img src="/assets/lectures/lab/html-css-puzzles/2-desk.jpg">
</a>

Make sure to adjust the type sizes, margins and padding at the mobile breakpoint.

<a href="/assets/lectures/lab/html-css-puzzles/2-mobile.jpg" target="_blank">
  <img src="/assets/lectures/lab/html-css-puzzles/2-mobile.jpg">
</a>

---

### 3. Flexible Checkerboard

<a href="/assets/lectures/lab/html-css-puzzles/3-desk.jpg" target="_blank">
  <img src="/assets/lectures/lab/html-css-puzzles/3-desk.jpg">
</a>

<a href="/assets/lectures/lab/html-css-puzzles/3-mobile.jpg" target="_blank">
  <img src="/assets/lectures/lab/html-css-puzzles/3-mobile.jpg">
</a>

---

### 4. Contain Yourself

<a href="/assets/lectures/lab/html-css-puzzles/4-desk.jpg" target="_blank">
  <img src="/assets/lectures/lab/html-css-puzzles/4-desk.jpg">
</a>

<a href="/assets/lectures/lab/html-css-puzzles/4-mobile.jpg" target="_blank">
  <img src="/assets/lectures/lab/html-css-puzzles/4-mobile.jpg">
</a>

---

### 5. Media Query Rothko

<a href="/assets/lectures/lab/html-css-puzzles/8-desk.jpg" target="_blank">
  <img src="/assets/lectures/lab/html-css-puzzles/8-desk.jpg">
</a>

<a href="/assets/lectures/lab/html-css-puzzles/8-mobile.jpg" target="_blank">
  <img src="/assets/lectures/lab/html-css-puzzles/8-mobile.jpg">
</a>

### 6. Typography and Google Font embed

<p>For this puzzle you'll need to use the <a href="https://fonts.google.com/specimen/Krona+One?selection.family=Krona+One">Krone One Google font</a> to match the screenshots. Click the "select font" button next to Krona One, then click on the "1 family selected" tab that appears at the bottom of your page. Follow the instructions to use the font in your CSS file.</p>
<p>For the example you'll also need to adjust the `letter-spacing`, `line-height`, and `font-size` properties to match the screenshots.</p>

<a href="/assets/lectures/lab/html-css-puzzles/9-desk.jpg" target="_blank">
  <img src="/assets/lectures/lab/html-css-puzzles/9-desk.jpg">
</a>

<a href="/assets/lectures/lab/html-css-puzzles/9-mobile.jpg" target="_blank">
  <img src="/assets/lectures/lab/html-css-puzzles/9-mobile.jpg">
</a>
