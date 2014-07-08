## Styling the Testimonials and Call-to-Action Sections

![Testimonials](https://bloc-books.s3.amazonaws.com/jottly/15-testimonials.png)

In this checkpoint we'll style the testimonial and call-to-action sections of our landing page. They're already positioned nicely, thanks to our grid layout, but now we want to make them look great.

### Testimonials

First we'll give the section some spacing at the top and bottom:

```css(stylesheets/base.css)
+/* Testimonials */
+#testimonials {
+ padding:4em 0;
+ text-align: center;
+}
```

Next, we'll style the header and paragraph text. We can use the same styles from our benefits section, since we're using the same color, font weights and size.

```css(stylesheets/base.css)
/* Testimonials */
#testimonials {
  padding:4em 0;
  text-align: center;
}
+
+#testimonials h2 {
+ color:#009be8;
+ font-weight: 300;
+}
+
+#testimonials p {
+ color:#9d9d9d;
+ font-size:1.2em;
+}
```

Skeleton comes with some default styles for blockquotes, however, we'll override those styles within this section:

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
+
+#testimonials blockquote {
+ border:none;
+ text-align: left;
+ padding:0 1.5em 0 0;
+ font-size:1em;
+ color:#4d4d4d;
+ line-height: 1.4;
+ margin-top: 1em;
+}
```

The default blockquote has a border, which we removed. Because we center-aligned of the text in this section with our original testimonials selector, we replaced that with a left-aligned value. We added some padding to the right side of the blockquotes for additional spacing as well.

Let's add a margin on the bottom to properly align our avatar and name:

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
  padding:0 1.5em 0 0;
  font-size:1em;
  color:#4d4d4d;
  line-height: 1.4;
  margin-top: 1em;
}
+
+#testimonials .avatar img {
+ border-radius: 50%;
+ float:left;
+ display:inline;
+ margin-right:1em;
+ width:65px;
+ height:65px;
+}
```

Rounded images for avatars are all the rage, so to do this we used a little CSS magic. Within our avatar class, we targeted the image and provided a border radius of 50%. To align the text with the avatar, we displayed these images inline and floated them to the left.

For the name next to the avatar, we'll assign a paragraph tag with a new font color and weight. This will center the text vertically with the avatar. We'll also provide some padding to the top of the text to push it down a bit:

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
+
+#testimonials .avatar p {
+ text-align: left;
+ padding-top:1.5em;
+ color:#5d5d5d;
+ font-weight: 900;
+}
```

### Call-to-Action

We'll add a new background image to this section with the background property. We'll align the image to the top of the container and center it horizontally:

```css(stylesheets/base.css)
+#action {
+ background:url('../images/action.jpg') top center no-repeat;
+ background-size: cover;
+ min-height: 180px;
+ width:100%;
+ padding:4em 0;
+ text-align: center;
+}
```

We set the width to fill 100%, and set the background size to "cover" so it scales with the section. For this to work, we also set a minimum height. Like the other sections, we added some padding to the top and bottom and centered our text.

Next, we'll reuse our styles from the pricing section for the header and paragraph text:

```css(stylesheets/base.css)
#action {
  background:url('../images/action.jpg') top center no-repeat;
  background-size: cover;
  min-height: 180px;
  width:100%;
  padding:4em 0;
  text-align: center;
}
+
+#action h2 {
+ color:#fff;
+ font-weight:300;
+ text-shadow: 0 1px 2px rgba(0,0,0,.2);
+}
+
+#action p {
+ color:#fff;
+ text-shadow: 0 1px 2px rgba(0,0,0,.2);
+ font-size:1.2em;
+}
```

Let's update the row class inside of this section. This is where our inputs reside, and we need to provide some spacing at the top:

```css(stylesheets/base.css)
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
}
+
+#action .row {
+ margin-top:3em;
+}
```

Next, we'll style the footer.
