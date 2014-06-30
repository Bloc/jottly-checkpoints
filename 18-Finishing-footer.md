## Finishing the footer

![Footer](http://cl.ly/WJPp/16-footer.png)

In this checkpoint, we're going to finish styling up the last section of our landing page: the footer.

To start with, we're going to target the `footer` div, changing the background and applying some padding to the top and bottom so we give it some ample spacing.

```css(stylesheets/base.css)
...
+/* Footer */
+#footer {
+	background:#009be8;
+	padding: 1em 0;
+}
```
	
Next, we're going to focus on fixing up our navigation on the left side. First, we must give it a little spacing on the top for room to breathe.

```css(stylesheets/base.css)
...
/* Footer */
#footer {
	background:#009be8;
	padding:1em 0;
}
+#footer nav ul {
+	margin-top:0.5em;
+}
+#footer nav ul li {
+	display:inline;
+	margin:0;
+}
```

Here, we've changed up the list items inside the unordered list to display inline. This will place them side-by-side to each other versus in list format. Now, we need to change the text color and a few other things.

```css(stylesheets/base.css)
...
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
+	color:#fff;
+	text-decoration:none;
+	text-transform: uppercase;
+	margin:0 1em 0 0;
+	font-size:1.1em;
+}
```

We've updated the color to white, removed the underline and made the links uppercase. We've also added in a margin on the right side while removing any other margins. We've also increased the font size just slightly so it appears slightly bigger on the blue background.

The last two items we need to style are the small logo and the copyright text.

```css(stylesheets/base.css)
...
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
+#footer img {
+	float:right;
+}
+#footer p {
+	color:#fff;
+	line-height: 1;
+	text-transform: uppercase;
+	font-size:0.7em;
+	margin-top:0.5em;
}
```

First, we've shifted the logo to the right using `float`. This will align the image to the right of the container its inside. With that, we've changed the copyright text to be white, following suit with being uppercase. We've also opted to minimize the size of the type so it can appear on two lines easier when viewing on desktop.

The slight margin we've add to the top lines up the text to the middle of the logo and provides a better baseline for all of the elements.

Now, we've finished with the hard stuff! You have updated code you need to push to Github Pages so you can view and share the results. 

The next few checkpoints are more for fun versus functionality. We're going to check out a simple way to add in animation to your site, giving it just a little extra.