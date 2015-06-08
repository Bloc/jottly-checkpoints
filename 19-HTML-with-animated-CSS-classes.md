## HTML with Animated CSS Classes

<center>![Animation](https://bloc-global-assets.s3.amazonaws.com/images-design/blocbooks/jottly/animate1.gif)</center>

In this checkpoint we'll add a subtle animation to our header to give it a nice effect when the page loads.

Since we've already incorporated the animate.css stylesheet, we can simply add a class to our header div:

```html(index.html)
<!-- Header	================================================== -->
- <header>
+ <header class="animated fadeInDown">
```

The animated class initiates the animation. The "fadeInDown" class fades the header div downwards when the page loads.

We'll add the same classes to the text within the header, so the div and text fade downward in unison.

```html(index.html)
- <div class="seven columns headertext">
+ <div class="seven columns headertext animated fadeInDown">
```

We'll experiment with one more animation before deploying Jottly.
