## Delaying Animation on text

![Delaying animation](http://cl.ly/WGkV/jottly-animate2.gif)

In this checkpoint we'll add one more animation effect to our header.

Within the base.css file, locate the headertext class. Within this selector, we'll add two simple classes to delay the text animation, so that the text animates after the main header. This will present a cool-looking effect when the page loads.

```css(stylesheets/base.css)
...
#header .headertext {
  margin-top: 10em;
+ animation-delay: 0.7s;
+ -webkit-animation-delay: 0.7s; /* Safari and Chrome */
}
 ...
```

Using CSS3 animation properties, we added an animation-delay and set it to happen just over a half of a second after the header animation. We added in an additional selector for Safari and Chrome consistency.

In the next checkpoint, we'll get setup with a Github account and find out how to manage your code.