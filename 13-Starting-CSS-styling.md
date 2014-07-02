## Starting to style the page

![](http://cl.ly/WHEI/12-header.png)

In this checkpoint we'll add our first custom CSS styles. We'll give the header a background image and adjust the spacing for our logo.

### Header Background

Within the base.css file, scroll to the bottom and insert a new comment.

A comment in CSS is defined with /* */ characters.

> Just like in HTML, comments can help keep your code organized.

```CSS(stylesheets/base.css)
+/* Sections
+================================================== */
+/* Header */
+#header {
+	background:url('../images/header.jpg') top center no-repeat;
+}
```

The first thing we've added is a property for background with a value of url('../images/header.jpg').

To include an image for your background, we have to define where it resides. In this case, it will be a URL. The path for our image is within the images folder. Because base.css is within a separate folder, we have to include the "../", which will move us up a level before looking for the images folder.

The last part of this value - "top center no-repeat" - defined the positioning of the image. This is considered shorthand CSS, by combining the following properties:

* background-image
* background-position: values such as top, center, bottom, left and right. You can combine a horizontal and a vertical position as shown above.
* background-repeat: there are four different values you can apply here: repeat -- tiles the image; repeat-y -- repeats vertically; repeat-x -- repeats horizontally; no-repeat -- only shows once.

This could also be written as:

```css
...{
  background-image:url('.../images/header.jpg');
  background-position: top center;
  background-repeat:no-repeat;
}
```

We can keep our code cleaner by adding it to the background property.

Let's size our image properly. We'll set the background-size to "cover" in order to fill the space. The cover value will scale the image to cover the background area. Portions of the image may be cut off in order to achieve this, but it gives us a full width effect nonetheless:

```CSS(stylesheets/base.css)
/* Sections
================================================== */
/* Header */
#header {
  background:url('../images/header.jpg') top center no-repeat;
+ background-size: cover;
+ min-height: 680px;
+ width:100%;
}
```

We added our width and set it to 100%. This will ensure the full page width is covered. We have also set a height and a minimum height requirement. We want the image to cover the majority of the browser window with a little space leftover, so we set this number to 680 pixels.

Finally, we'll add a touch of margin to space our logo away from the top of the browser window:

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
+  margin-top: 1em;
+}
```

CSS allows us to use pixels, ems, percentages and even points as a means of measurement. You'll notice that we use em as our default for Jottly.

### Pushing your changes

Push your changes to Github:

```bash(Terminal)
$ git add .
$ git commit -m "Styled the landing image"
$ git push origin gh-pages
```

Next, we'll finish all the styling for our header, including adjusting the navigation.
