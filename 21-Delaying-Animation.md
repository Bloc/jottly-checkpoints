## Delaying Animation on text

![Delaying animation](http://cl.ly/WGkV/jottly-animate2.gif)

In this checkpoint, we're going to add one more animation effect to our header, finishing it up for publishing.

Within our `base.css` file, locate the line where your class `headertext` appears. Within this selector, we're going to add two simple classes to delay the animation, so that the text animates after the main header.

```css(stylesheets/base.css)
...
#header .headertext {
	margin-top: 10em;
+	animation-delay: 0.7s;
+	-webkit-animation-delay: 0.7s; /* Safari and Chrome */
 }
 ...
```

Using CSS3 animation properties, we add in the `animation-delay` and set it to happen just over a half of a second after. We added in an additional selector to target Safari and Chrome.

### Github

The last step to finishing this project is to push your changes to your Github Pages repo. Open up Terminal, and follow the commands you've used throughout these checkpoints.

```bash(Terminal)
$ git add .
$ git commit -m "Removed default content"
$ git push
```

And there you have it! You have completed your first HTML and CSS landing page. Congratulations!
