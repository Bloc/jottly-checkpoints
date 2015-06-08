## Animating CSS

<center>![Animate CSS](https://bloc-books.s3.amazonaws.com/jottly/19-animate.png)</center>

In this checkpoint we'll download and add [Animate.css](http://daneden.github.io/animate.css/) to our source code.

[Animate.css](https://raw.github.com/daneden/animate.css/master/animate.css) was created by [Dan Eden](http://daneden.me/) and open-sourced for anyone to use in their projects.

Create a new file in your Jottly/css folder named `animate.css`. [Open the `animate.css` source file](https://raw.github.com/daneden/animate.css/master/animate.css) and copy and paste it into the `animate.css` file you just created.

Now we'll reference the new animate.css file in `index.html`. This will allow us to use animations via classes on HTML elements.

```html(index.html)
  <link rel="stylesheet" href="css/normalize.css">
  <link rel="stylesheet" href="css/skeleton.css">
+ <link rel="stylesheet" href="stylesheets/animate.css">
```

Let's move on to experiment with some animations.
