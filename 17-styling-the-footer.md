## Styling the Footer

![Footer](https://bloc-books.s3.amazonaws.com/jottly/16-footer.png)

In this checkpoint we'll style the last section of our landing page - the footer.

Let's change the background of the footer div and apply some padding to the top and bottom:

```css(stylesheets/base.css)
+/* Footer */
+#footer {
+ background:#009be8;
+ padding: 1em 0;
+}
```

Next we'll update the navigation on the left side. Let's give it a little spacing on the top:

```css(stylesheets/base.css)
/* Footer */
#footer {
  background:#009be8;
  padding:1em 0;
}
+
+#footer nav ul {
+ margin-top:0.5em;
+}
+
+#footer nav ul li {
+ display:inline;
+ margin:0;
+}
```

We changed the list items inside the unordered list to display inline. This will place them side-by-side instead of vertically.

Next we'll change some text properties:

```css(stylesheets/base.css)
/* Footer */
#footer {
  background:#009be8;
  padding:1em 0;
}

#footer nav ul {
  margin-top:0.5em;
}

#footer nav ul li {
  display:inline;
  margin:0;
}

+#footer nav ul li a {
+ color:#fff;
+ text-decoration:none;
+ text-transform: uppercase;
+ margin:0 1em 0 0;
+ font-size:1.1em;
+}
```

We've updated the text color to white, removed the underline and made the links uppercase. We also added a margin on the right side while removing the other margins. We increased the font size slightly so it appears bigger on the blue background.

The last two items we need to style are the small logo and the copyright text:

```css(stylesheets/base.css)
/* Footer */
#footer {
  background:#009be8;
  padding:1em 0;
}

#footer nav ul {
  margin-top:0.5em;
}

#footer nav ul li {
  display:inline;
  margin:0;
}

#footer nav ul li a {
  color:#fff;
  text-decoration:none;
  text-transform: uppercase;
  margin:0 1em 0 0;
  font-size:1.1em;
}
+
+#footer img {
+ float:right;
+}
+
+#footer p {
+ color:#fff;
+ line-height: 1;
+ text-transform: uppercase;
+ font-size:0.7em;
+ margin-top:0.5em;
+}
```

We shifted the logo to the right using a float. The float will align the image to the right of the container it's inside. We changed the copyright text to be white and uppercase. We opted to minimize the size of the type so it appears on two lines. This should make it more readable.

Now our landing page is complete and beautiful! The sections are distinct, the page flows well and we've made sure that the most important information is highlighted.

In the final checkpoints we'll implement some subtle animation to make Jottly sizzle, and deploy it so we can share it with the world.
