## Starting to style the page

![](http://cl.ly/WHEI/12-header.png)

In this checkpoint, we're going to begin adding some styles to our CSS file. We'll start with the header by giving it a background image, and adjusting the spacing for our logo.

### Header Background

First, we're going to add a background image to the `header` div. Within our `base.css` file, scroll down to the bottom and begin a new comment. Within CSS, a comment is defined by `/* Add comment here */`. Be sure to close the comment with `*/`, or it will comment out your styles, which wouldn't render them.

> Just like in HTML, comments are great to add in to quickly sections of code. Comments can also keep your code organized.


```CSS(stylesheets/base.css)
+/* Sections
+================================================== */
+/* Header */
+#header {
+	background:url('../images/header.jpg') top center no-repeat;
+}
```

The first thing we've add is a property for `background`. Next we add in the value of `url('../images/header.jpg)`. In CSS, to include an image for your background, you have to define where it resides. In this case, it will be a URL. And the path to that image is within the `images` folder in our directory. Because `base.css` is within a separate folder, we have to include the `../`. This snippet takes us one level out of our current folder (which is `stylesheets`) to the main directory level, and then the path drops us into the `images` folder and pinpoints our selected image.

The last portions of this value define the positioning of the image itself. This is considered shorthand CSS. This could also be written in the longform, like:

```css
...{
	background-image:url('.../images/header.jpg);
	background-position: top center;
	background-repeat:no-repeat;}
```

To save us time, we can condense it to just the `background` property. The `no-repeat` value refers to the image being repeated multiple times to fill the container it's within, and in this case, we don't want it to repeat.

Next, we're going to focus on getting the image sized properly. 

We're going to set our `background-size` to `cover` in order to fill the space. The `cover` value will scale the image to cover the background area. Portions of the image may be cut off in order to achieve this, but it gives us the full width effect we're going for.

```CSS(stylesheets/base.css)
/* Sections
================================================== */
/* Header */
#header {
	background:url('../images/header.jpg') top center no-repeat;
+	background-size: cover;
+	min-height: 680px;
+	width:100%;
}
```

With that, we add in our width and set it to 100%. This will ensure the full page width is covered. And we have to set a height, in this case, and minimum height requirement. We want it to cover the majority of the browser window, but leaving some room. So we've set this number to 680 pixels.

Finally, we're going to add a touch of margin to space out our logo from the top of the browser window.

```CSS(stylesheets/base.css)
/* Sections
================================================== */
/* Header */
#header {
	background:url('../images/header.jpg') top center no-repeat;
	background-size: cover;
	min-height: 680px;
	width:100%;
}
+#header .logo {
+	margin-top: 1em;
+}
```

Within CSS, you can use pixels, ems, percentages and even points as a means of measurement. You'll notice through these checkpoints, we use `em` as our default. If you want to read more on the difference, check out [this post](http://kyleschaeffer.com/development/css-font-size-em-vs-px-vs-pt-vs/). It discusses in terms of font sizing, however, it's applicable to spacing as well.

Next, we're going to move onto finishing all the styling for our header, including adjusting the navigation.