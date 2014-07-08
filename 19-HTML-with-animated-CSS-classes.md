## HTML with Animated CSS Classes

![Animation](https://bloc-books.s3.amazonaws.com/jottly/jottly-animate1.gif)

In this checkpoint we'll add a subtle animation to our header to give it a nice effect when the page loads.

Since we've already incorporated the animate.css stylesheet, we can simply add a class to our header div:

```html(index.html)
<!-- Header	================================================== -->
- <div id="header">
+ <div id="header" class="animated fadeInDown">
```

The animated class initiates the animation. The "fadeInDown" class fades the header div downwards when the page loads.

We'll add the same classes to the text within the header, so the div and text fade downward in unison.

```html(index.html)
- <div class="nine columns headertext">
+ <div class="nine columns headertext animated fadeInDown">
```

We'll experiment with one more animation before deploying Jottly.
