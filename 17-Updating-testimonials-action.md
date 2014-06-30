## Updating the testimonials and action sections

![Testimonials](http://cl.ly/WLuF/15-testimonials.png)

In this checkpoint, we're going to style the testimonials section of our landing page. We've already set them up in three equal columns across the page, but want to change the look just slightly.

### Testimonials

First, we'll start off by giving the section some spacing at the top and bottom.

```css(stylesheets/base.css)
...
+/* Testimonials */
+#testimonials {
+	padding:4em 0;
+	text-align: center;
+}
```

Next, we're going to style the header and paragraph text. We can use the same styles from our benefits section, as we're using the same color, font weights and size.

```css(stylesheets/base.css)
/* Testimonials */
#testimonials {
	padding:4em 0;
	text-align: center;
}
+#testimonials h2 {
+	color:#009be8;
+	font-weight: 300;
+}
+#testimonials p {
+	color:#9d9d9d;
+	font-size:1.2em;
+}
```

Skeleton comes with some pre-defined styles for blockquotes, however, we're going to override those styles here by targeting the blockquotes within this section directly.

```css(stylesheets/base.css)
/* Testimonials */
#testimonials {
	padding:4em 0;
	text-align: center;
}
#testimonials h2 {
	color:#009be8;
	font-weight: 300;
}
#testimonials p {
	color:#9d9d9d;
	font-size:1.2em;
}
+#testimonials blockquote {
+	border:none;
+	text-align: left;
+	padding:0 1.5em 0 0;
+	font-size:1em;
+	color:#4d4d4d;
+	line-height: 1.4;
+	margin-top: 1em;
+}
```

It currently has a border, which we've removed. Because we've center-aligned all of the text in this section in our original `#testimonials` selector, we are again going to override that to align to the left. We've added some padding to the right side of the quotes just for additional spacing, and provided a margin on the bottom to properly align our avatar and name that will go below.

```css(stylesheets/base.css)
/* Testimonials */
#testimonials {
	padding:4em 0;
	text-align: center;
}
#testimonials h2 {
	color:#009be8;
	font-weight: 300;
}
#testimonials p {
	color:#9d9d9d;
	font-size:1.2em;
}
#testimonials blockquote {
	border:none;
	text-align: left;
	padding:0 1.5em 0 0;
	font-size:1em;
	color:#4d4d4d;
	line-height: 1.4;
	margin-top: 1em;
}
+#testimonials .avatar img {
+	border-radius: 50%;
+	float:left;
+	display:inline;
+	margin-right:1em;
+	width:65px;
+	height:65px;
+}
```

Rounded images for avatars are all the rage, so to do this, we use a little CSS magic. Within our `.avatar` class, we target the image and provide a border radius of 50%. In order to line up the text next to the avatar, we display these images inline and float them to the left. We've also set a width and height so they appear the way we'd like them to.

```css(stylesheets/base.css)
/* Testimonials */
#testimonials {
	padding:4em 0;
	text-align: center;
}
#testimonials h2 {
	color:#009be8;
	font-weight: 300;
}
#testimonials p {
	color:#9d9d9d;
	font-size:1.2em;
}
#testimonials blockquote {
	border:none;
	text-align: left;
	padding:0 1.5em 0 0;
	font-size:1em;
	color:#4d4d4d;
	line-height: 1.4;
	margin-top: 1em;
}
#testimonials .avatar img {
	border-radius: 50%;
	float:left;
	display:inline;
	margin-right:1em;
	width:65px;
	height:65px;
}
+#testimonials .avatar p {
+	text-align: left;
+	padding-top:1.5em;
+	color:#5d5d5d;
+	font-weight: 900;
+}
```

For the name next to the avatar, we've assigned a paragraph tag, which we have changed the color and font weight. So it appears to center vertically with the avatar, we provide some padding to the top of the text to push it down.

Next, we're going to take a look at the action section.

### Action

First, we're going to add a new background image to this section within your `images` folder called `action.jpg`.

We start by adding the `background` property, aligning the image to the top of the container and centered horizontally. We don't want it to repeat.

```css(stylesheets/base.css)
...
+#action {
+	background:url('../images/action.jpg') top center no-repeat;
+	background-size: cover;
+	min-height: 180px;
+	width:100%;
+	padding:4em 0;
+	text-align: center;
+}
```

We set the width to fill 100%, and set the background size to `cover` so it scales with the section. For this to work, we also set a minimum height. Like the other sections, we've added some padding to the top and bottom, and aligned our text to the center.

Next, we can reuse our styles from the pricing section for the header and paragraph text.

```css(stylesheets/base.css)
...
#action {
	background:url('../images/action.jpg') top center no-repeat;
	background-size: cover;
	min-height: 180px;
	width:100%;
	padding:4em 0;
	text-align: center;
}
+#action h2 {
+	color:#fff;
+	font-weight:300;
+	text-shadow: 0 1px 2px rgba(0,0,0,.2);
+}
+#action p {
+	color:#fff;
+	text-shadow: 0 1px 2px rgba(0,0,0,.2);
+	font-size:1.2em;
+}
```

The last thing we want to do is target the `.row` class inside of this section. This is where our inputs reside, and we need to provide some spacing to the top so it's not directly below our text above it.

```css(stylesheets/base.css)
...
#action {
	background:url('../images/action.jpg') top center no-repeat;
	background-size: cover;
	min-height: 180px;
	width:100%;
	padding:4em 0;
	text-align: center;
}
#action h2 {
	color:#fff;
	font-weight:300;
	text-shadow: 0 1px 2px rgba(0,0,0,.2);
}
#action p {
	color:#fff;
	text-shadow: 0 1px 2px rgba(0,0,0,.2);
	font-size:1.2em;
+}
+#action .row {
+	margin-top:3em;
}
```

As we've already adjusted the inputs for our header section, we don't have to worry about redoing these, as they will take hold globally on our page.

Next, we're going to finish up the footer so our page is complete!