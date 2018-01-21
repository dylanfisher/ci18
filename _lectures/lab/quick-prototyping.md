---
title:            Quick Prototyping
lecture_date:     2017-04-26 00:00:00 -0500
section:          Lab
hidden:           true
---

### Instructions

1. Download the [starter kit](/assets/lectures/lab/quick-prototyping/quick_prototyping.zip).
1. For each task you'll have approximately 30 minutes to quickly prototype a design using HTML, CSS and jQuery.
1. At the end of each task, push your code to GitHub so that we can review as a group.
1. Copy the starter kit and edit the files in the directory corresponding to the excercise question.
1. These prompts are all very open ended. Have fun with quick prototyping!

---

### 1. Creative Breakpoints

- Use breakpoints in a creative way, including at least one breakpoint that targets devices in landscape orientation.
- Include at least 4 different breakpoints.
- Make something drastic and/or unexpected happen at each breakpoint.

```css
@media (orientation: landscape) {
  /* CSS that's applied only to phones
     in landscape orientation */
}
```

To target other breakpoints, you may use code such as:

```css
@media (max-width: 600px) {
  /* Something that happens when the
     browser is at least 600px wide */
}

@media (max-width: 700px) {
  /* Something that happens when the
     browser is at least 700px wide */
}
```

---

### 2. Responding to Time

- Use JavaScript to insert the current time and/or day on the page.
- Use CSS to style it
- View this CodePen for more inspiration [https://codepen.io/dylanfisher/pen/zwojOq?editors=1010](https://codepen.io/dylanfisher/pen/zwojOq?editors=1010)
- Think about how can time be represented in new and different ways in the context of a website.

```html
<div id="time"></div>
```

```js
function updateTime() {
  var date = new Date();
  $('#time').html( date.toGMTString() );
}

$(function() {
  updateTime();
  setInterval(updateTime, 1000);
});
```

References

- [aspenartmuseum.org](https://www.aspenartmuseum.org/) the font weight changes each season.
- [arch.columbia.edu](https://www.arch.columbia.edu/) font weights and other aspects of the design change throughout the day.
- [chambernyc.com](https://chambernyc.com/) large presence of analogue display clock.
- [nikasimovich.com](http://nikasimovich.com/) layout and design change following phases of the moon; has a screensaver mode.

---

### 3. Immersive Experiences

- Create an immersive web experience using a video or other media item.
- Try juxtaposing the content in the background with content in the foreground.
- [https://codepen.io/dylanfisher/pen/QvGrNX](https://codepen.io/dylanfisher/pen/QvGrNX)
- [YouTube Embedded Players and Player Parameters](https://developers.google.com/youtube/player_parameters)

It's easy to use existing media services such as YouTube and Vimeo in creative ways.

References

- [http://so-il.org/](http://so-il.org/)
- [http://astronaut.io/](http://astronaut.io/)
- [http://psfa-bxl.org/](http://psfa-bxl.org/)
- [http://hakunamatata.house/](http://hakunamatata.house/)

---

### 4. Location

- Embedding a Google map in an iframe is easy.
- [https://codepen.io/dylanfisher/pen/XRNqya?editors=1100](https://codepen.io/dylanfisher/pen/XRNqya?editors=1100)
- To further customize an embedded map, you must use the Google Maps JavaScript API.
- [https://mapstyle.withgoogle.com/](https://mapstyle.withgoogle.com/)

Location can be thought about in terms of maps, images or other devices. You don't necessarily
need to use an embedded map. If you do, try use it in a creative way. For example, the 9-Eyes project
by Jon Rafman below.

References

- [9-Eyes, Jon Rafman](http://9-eyes.com/)
- [http://www.sashaportis.com/forward/forward.html](http://www.sashaportis.com/forward/forward.html)
- [https://www.arch.columbia.edu/earth](https://www.arch.columbia.edu/earth)
- [http://www.postcards-from-google-earth.com/](http://www.postcards-from-google-earth.com/)
