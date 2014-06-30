## Styling the Pricing Tiers

![](http://cl.ly/WHKa/14-pricing.png)

In this checkpoint, we will style the pricing section. We'll focus on getting the text adjusted just right to display nicely, and get our boxes looking similar to each other, with some minor adjustments to our box in the center.

### Base styles

Before we tackle the price boxes, we need to set up the section itself. We want to change the background to blue, but in order for the content to appear nicely, we also need to add some padding. 

While we're at it, we'll have to adjust the color of the header and paragraph text, since it will be too dark to render on here.

```css(stylesheets/base.css)
+/* Pricing */
+#pricing {
+	background:#009be8;
+	padding:4em 0;
+	text-align: center;
+}
+#pricing h2 {
+	color:#fff;
+	font-weight:300;
+	text-shadow: 0 1px 2px rgba(0,0,0,.2);
+}
+#pricing p {
+	color:#fff;
+	text-shadow: 0 1px 2px rgba(0,0,0,.2);
+	font-size:1.2em;
+}
```

We've added a text shadow to the `h2` and `p` tags just to help them pop off the page. 

### Price Box

Within our HTML, we have a `pricebox` div. This houses our pricing content, so we are going to change the background color to white so it contrasts nicely with the blue background. 

```css(stylesheets/base.css)
/* Pricing */
#pricing {
	background:#009be8;
	padding:4em 0;
	text-align: center;
}
#pricing h2 {
	color:#fff;
	font-weight:300;
	text-shadow: 0 1px 2px rgba(0,0,0,.2);
}
#pricing p {
	color:#fff;
	text-shadow: 0 1px 2px rgba(0,0,0,.2);
	font-size:1.2em;
}
+.pricebox {
+	background-color: #fff;
+	-moz-box-shadow: 0 1px 3px rgba(0,0,0,.2);
+	-webkit-box-shadow: 0 1px 3px rgba(0,0,0,.2);
+	box-shadow: 0 1px 3px rgba(0,0,0,.2);
+	margin-top:3em;
+	height:400px;
+	position: relative;
+}
```

We've added a box shadow to give the price boxes a layering effect. Here, we've used browser prefixes to ensure this appears in Mozilla, Chrome, Safari and other modern browsers. Much like the text shadow, the box shadow syntax is broken down as such:

```css
box-shadow: horizontal vertical blur color;
```

We've also set the height of the box, as we'll use this in the next portion of the CSS. Also, we've added a position property and set it to relative. This will come in handy with some positioning for our other elements.

### Differentiating Price Boxes

For our second box — Small Busineses — we are going to add in a second class of `deal` to the `pricebox` div inside the HTML file. We're doing this so we can differentiate the middle box from the other two.

```html(index.html)
 ...
			<div class="one-third column">
 -				<div class="pricebox">
 +				<div class="pricebox deal">
					<header>
						<h3>Small Businesses</h3>
					</header>
					<section>
...
```

Now, we can add in a new class selector to our `base.css` targeting the pricebox and deal classes. We've minimized the top margin so it stands taller than the others. We've also adjusted the height so it extends down further as well.

```css(stylesheets/base.css)
...
#pricing p {
	color:#fff;
	text-shadow: 0 1px 2px rgba(0,0,0,.2);
	font-size:1.2em;
}
.pricebox {
	background-color: #fff;
	-moz-box-shadow: 0 1px 3px rgba(0,0,0,.2);
	-webkit-box-shadow: 0 1px 3px rgba(0,0,0,.2);
	box-shadow: 0 1px 3px rgba(0,0,0,.2);
	margin-top:3em;
	height:400px;
	position: relative;
}
+.pricebox.deal {
+	margin-top:2em;
+	height:430px;
+}
```

### Header

For the header containing our `h3` text, we're going to change up the background, add a small box shadow and adjust the padding.

```css(stylesheets/base.css)
...
.pricebox {
	background-color: #fff;
	-moz-box-shadow: 0 1px 3px rgba(0,0,0,.2);
	-webkit-box-shadow: 0 1px 3px rgba(0,0,0,.2);
	box-shadow: 0 1px 3px rgba(0,0,0,.2);
	margin-top:3em;
	height:400px;
	position: relative;
}
.pricebox.deal {
	margin-top:2em;
	height:430px;
}
+.pricebox header {
+	background-color: #f1f1f1;
+	-moz-box-shadow: 0 1px 3px rgba(0,0,0,.2);
+	-webkit-box-shadow: 0 1px 3px rgba(0,0,0,.2);
+	box-shadow: 0 1px 3px rgba(0,0,0,.2);
+	padding:1em 0;
+	margin-bottom:2em;
+}
+.pricebox header h3 {
+	color:#4d4d4d;
+	font-size:1.4em;
+	text-transform: uppercase;
+	margin:0;
+	font-weight: 600;
+}
```

We've also changed up the `h3` text styles so it all uppercase and thicker. We've increased the size to give it some prominence.

### Buttons

With our button, we've changed the color to a shade of green. We've are positioning it to always be at the bottom of the price box, spaced 1em from the bottom edge, no matter what height the box is. This will cleanly align the two outer buttons, and keeps the spacing consistent in the middle box as well.

```css(stylesheets/base.css)
...
.pricebox header {
	background-color: #f1f1f1;
	-moz-box-shadow: 0 1px 3px rgba(0,0,0,.2);
	-webkit-box-shadow: 0 1px 3px rgba(0,0,0,.2);
	box-shadow: 0 1px 3px rgba(0,0,0,.2);
	padding:1em 0;
	margin-bottom:2em;
}
.pricebox header h3 {
	color:#4d4d4d;
	font-size:1.4em;
	text-transform: uppercase;
	margin:0;
	font-weight: 600;
}
+.pricebox section button {
+	background:#2ecc71;
+	position:absolute;
+	bottom:1em;
+	width:90%;
+	left:0;
+	right:0;
+	margin:0 auto;
+	text-align: center;
+}
+.pricebox section button:hover {
+	background:#1fae5c;
+}
+.pricebox section h4 {
+	display:inline-block;
+	color:#009be8;
+	font-size: 6em;
+	font-weight: 900;
+	vertical-align: bottom;
+}
```

We set the width to 90% of the button so it doesn't hit the outer edges of the box. And adding in a margin of `0 auto`, it centers our element inside the box.

### Price Text

For the price of our services in Jott.ly, we want to increase the text size to give it prominence over the rest of the content inside each of the boxes.

```css(stylesheets/base.css)
...
.pricebox section button:hover {
	background:#1fae5c;
}
+.pricebox section h4 {
+	display:inline-block;
+	color:#009be8;
+	font-size: 6em;
+	font-weight: 900;
+	vertical-align: bottom;
+}
```

Here, we've changed the color and size. Before we go further, we want to update some of our HTML so that we can adjust the size and baseline of the `$` within the price. We're going to add a `span` around the dollar symbol, and then provide a break between 'per month' and '/per user' so it appears on two lines.

Go ahead and do this inside your `index.html` for all three boxes.

```html(index.html)
...
 						<h3>Individuals &amp; Family</h3>
  					</header>
  					<section>
-						<h4>$2</h4>
-						<p>per month/per user</p>
+						<h4><span>$</span>2</h4>
+						<p>per month<br/>/per user</p>
  						<ul>
  							<li>Unlimited notes</li>
  							<li>Unlimited members</li>
...
  			<div class="one-third column">
				<div class="pricebox deal">
  					<header>
  						<h3>Small Businesses</h3>
  					</header>
  					<section>
-						<h4>$5</h4>
-						<p>per month/per user</p>
+						<h4><span>$</span>5</h4>
+						<p>per month<br/>/per user</p>
  						<ul>
  							<li>Unlimited notes</li>
  							<li>Unlimited members</li>
...
   						<h3>Enterprise</h3>
  					</header>
  					<section>
-						<h4>$8</h4>
-						<p>per month/per user</p>
+						<h4><span>$</span>8</h4>
+						<p>per month<br/>/per user</p>
  						<ul>
  							<li>Unlimited notes</li>
  							<li>Unlimited members</li>
...
```

Now that we've added that to our HTML, we can adjust the styling so it appears just right.

With our primary `h4` size being 6em, we want to adjust the span inside of it to be half of that. If you enter `3em` for the font size, you will see it massively larger than that of the price itself. This is because that number will multiply the number above it, meaning 6em x 3 em = too big. So we want to multiply it by 0.5em, so it minimizes in size.

```css(stylesheets/base.css)
...
.pricebox section button:hover {
	background:#1fae5c;
}
.pricebox section h4 {
	display:inline-block;
	color:#009be8;
	font-size: 6em;
	font-weight: 900;
	vertical-align: bottom;
}
+.pricebox section h4 span {
+	font-size:0.5em;
+	line-height: 1;
+	vertical-align: top;
+}
+#pricing .pricebox section p {
+	display:inline-block;
+	color:#9d9d9d;
+	text-shadow:none;
+	line-height: 1;
+	position:relative;
+	top:1em;
+	font-size:1.1em;
+}
```

To adjust the baseline, we've added a vertical alignment property, moving it to the top which will align the top edges of the `$` and the numeral. Next, we've updated the look of our 'per month/per user' text. We display this content `inline-block` so it will adjust to the right of the price. We have to remove the text shadow, as we added one earlier to target all things tagged `p` inside this section. After updating the color, we adjust the positioning to give it some spacing at the top, pushing it down to line up in the center vertically with the price.

> Using Inspect Element inside Chrome, you are able to adjust the CSS of your files to test out and adjust to get your elements lined up just right. Be sure to edit your files though, as any changes you make in Inspect Element will not save.

### List of Features

The last part of our price boxes we want to edit are the lists of features.

For our unordered list, we add in some margin to the top so it's not bumped right up against the price. And then for each list item, we've slightly adjusted the text size and provided some additional spacing in between each one so it's easier to scan and read.

```css(stylesheets/base.css)
...
.pricebox section h4 span {
	font-size:0.5em;
	line-height: 1;
	vertical-align: top;
}
#pricing .pricebox section p {
	display:inline-block;
	color:#9d9d9d;
	text-shadow:none;
	line-height: 1;
	position:relative;
	top:1em;
	font-size:1.1em;
}
+.pricebox section ul {
+	margin-top:3em;
+}
+.pricebox section ul li {
+	font-size:1.2em;
+	margin-bottom: 1.2em;
}
```

Now, your `index.html` file should resemble that of the nearly finished product. Next, we'll work on updating the testimonials and action sections.