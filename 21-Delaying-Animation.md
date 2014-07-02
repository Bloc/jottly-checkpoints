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

### Pushing your changes

Push your changes to Github:

```bash(Terminal)
$ git add .
$ git commit -m "Delayed text animation"
$ git push origin gh-pages
```

Congratulations! You have completed your first landing page and learned a lot about HTML and CSS in the process. Jottly is now ready to accept customers, once you've created the actual product :)
