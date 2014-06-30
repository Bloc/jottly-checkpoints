## Styling the header

![](http://cl.ly/WHHY/12-style-header.png)

In this checkpoint, we're going to update the styling of the navigation, the text and the input field with submit button.

### Navigation

First, we're going to add a simple class to the second list item in our navigation. We are doing this simply because the style of the button is different from that of the other.

```html(index.html)
...
<nav>
     <ul>
          <li><a href="#">Sign In</a></li>
-         <li><a href="#">Sign Up Now</a></li>
+         <li><a class="btn" href="#">Sign Up Now</a></li>
     </ul>
</nav>
...  
```

We've added a class called `btn` to the anchor tag, in which we'll style in our CSS file. First, we're going to focus on getting the navigation to appear on the right side of the page.

To align text, you simply add the property `text-align` and shift to the right. We've also added a small margin to the top of the navigation to push it down the page so it's not being cut off by the browser window.

```CSS(stylesheets/base.css)
+#header nav {
+	text-align:right;
+	margin-top:2em;
+}
+#header nav ul li {
+	display:inline-block;
+}
```
 
We have an unordered list and list items nested within our nav. So we structured our CSS to go from selector to selector down the HTML content. When we target those list items, we want them to appear inline with each other. For this, we use the `display` property and set the value to `inline-block`.

Next, we're going to adjust the padding, color and text qualities of the links to meet our final product mockup.
	
```CSS(stylesheets/base.css)
#header nav {
	text-align:right;
	margin-top:2em;
}
#header nav ul li {
	display:inline-block;
}
+#header nav ul li a {
+	color:#fff;
+	text-transform:uppercase;
+	text-decoration:none;
+	padding:0.75em 2em;
+}
```
 
In order to change the color of the text, we target the anchor tag within the list items, and set the color to white, which is `#fff` in hexidecimal value. We set the word to be `uppercase` by transforming the text. And we remove the underline by giving the `text-decoration` property a value of `none`. 
	
```CSS(stylesheets/base.css)
#header nav {
	text-align:right;
	margin-top:2em;
}
#header nav ul li {
	display:inline-block;
}
#header nav ul li a {
	color:#fff;
	text-transform:uppercase;
	text-decoration:none;
	padding:0.75em 2em;
}
+#header nav ul li a.btn {
+	-moz-border-radius: 8px;
+	-webkit-border-radius: 8px;
+	border-radius: 8px; /* border radius */
+	border:2px solid #fff;
+}
+#header nav ul li a.btn:hover {
+	background:#fff;
+	color:#009be8;
+}
```

With these new additions, we're targeting that `btn` class we added to our `index.html` file earlier. We want to have a rounded box around the text to form a nice, clean button.

We've added a border radius, and as you see, there are three different syntaxes that do this. We add these vendor-prefixes for multiple browsers, like `-moz`, which targets Mozilla's Firefox, and `-webkit`, which targets Chrome and Safari.

### Text

Now, we're going to focus our attention to fixing up the text on top of the header image. Before we begin styling, let's go ahead and add a new class to our 9-column element in the HTML file.

```html(index.html)
...
<div class="container">
-    <div class="nine columns">
+    <div class="nine columns headertext">
          <h1>An easier way to write &amp; collaborate</h1>
          <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
...
```

Within our `base.css`, we can begin adding our selectors to target each element and begin styling our text. We'll start with spacing the entire box down the page so it's got some breathing room.

```css(stylesheets/base.css)
+#header .headertext {
+	margin-top: 10em;
+}
```

Next, we'll change the color, font weight, sizing and other qualities of our `h1`. First, we're going to set the text to render white. We want a thinner font, so we use the `font-weight` property and give it a value of `300`.

```css(stylesheets/base.css)
#header .headertext {
	margin-top: 10em;
}
+#header h1 {
+	color:#fff;
+	font-weight:300;
+	font-size:4.5em;
+	line-height: 1;
+	text-shadow: 0 1px 2px rgba(0,0,0,.2);
+	margin-bottom: 0.3em;
+}
```

We have increased the size to `4.5em`, which scales it to fit nicely in our columns. The `line-height` determines the spacing between lines. The value of `1` keeps the lines nice and tight together without overlapping. Next, we've added in a text shadow to help the text pop off the background and provide some depth.

Text shadows are broken down by the following:

```css
text-shadow { horizontal vertical blur color}
```
	
For this, we're setting the horizontal shadow to 0, vertical to 1 and blur to 2. The color, we're setting in RGBA, which gives you the ability to add some transparency or opacity to the color. `0,0,0` in RGB equals black, and we've drawn it back to be only 20% opaque. 

Next, we're going to update the properties of the paragraph text below the `h1`.

```css(stylesheets/base.css)
#header .headertext {
	margin-top: 10em;
}
#header h1 {
	color:#fff;
	font-weight:300;
	font-size:4.5em;
	line-height: 1;
	text-shadow: 0 1px 2px rgba(0,0,0,.2);
	margin-bottom: 0.3em;
}
+#header p {
+	color:#d5d5d5;
+	font-size:1.33em;
+	line-height: 1.5;
+	text-shadow: 0 1px 2px rgba(0,0,0,.2);
+	margin-bottom: 1.2em;
+}
+#header p strong {
+	color:#fff;
+}
```

Just like before, we updated the color to a light gray. We've updated the font size to increase slightly larger than the normal amount. The `line-height` here we've set to be 1.5 to allow for easier readability between the lines of text in this block. Again, we've added a slight text shadow, and set a margin below this element.

Because we have a `strong` tag inside our `p` tag, we've decided to lighten the text from the rest and make it pure white.

Next, we're going to take a look at the input field, the submit button and the second section of our site.