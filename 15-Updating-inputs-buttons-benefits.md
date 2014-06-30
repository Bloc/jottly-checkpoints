## Updating Styles for the input field, buttons and Benefits

![Input and Button](http://cl.ly/WHKo/13-input.png)

In this checkpoint, we're going to create some new styles for our input field, buttons as well as the Benefits section of the Jott.ly landing page.

### Input fields and buttons

Skeleton comes with pre-defined styles for inputs and buttons. We need to remove these so we can style ours appropriately. So locate the submit input styles in your `base.css` file, and remove all of the properties and values within them.

```CSS(stylesheets/base.css)
...
input[type="submit"],
input[type="reset"],
input[type="button"] {
-	background: #eee; /* Old browsers */
-	background: #eee -moz-linear-gradient(top, rgba(255,255,255,.2) 0%, rgba(0,0,0,.2) 100%); /* FF3.6+ */
-	background: #eee -webkit-gradient(linear, left top, left bottom, color-stop(0%,rgba(255,255,255,.2)), color-stop(100%,rgba(0,0,0,.2))); /* Chrome,Safari4+ */
-	background: #eee -webkit-linear-gradient(top, rgba(255,255,255,.2) 0%,rgba(0,0,0,.2) 100%); /* Chrome10+,Safari5.1+ */
-	background: #eee -o-linear-gradient(top, rgba(255,255,255,.2) 0%,rgba(0,0,0,.2) 100%); /* Opera11.10+ */
-	background: #eee -ms-linear-gradient(top, rgba(255,255,255,.2) 0%,rgba(0,0,0,.2) 100%); /* IE10+ */
-	background: #eee linear-gradient(top, rgba(255,255,255,.2) 0%,rgba(0,0,0,.2) 100%); /* W3C */
-	border: 1px solid #aaa;
-	border-top: 1px solid #ccc;
-	border-left: 1px solid #ccc;
-	-moz-border-radius: 3px;
-	-webkit-border-radius: 3px;
-	border-radius: 3px;
-	color: #444;
-	display: inline-block;
-	font-size: 11px;
-	font-weight: bold;
-	text-decoration: none;
-	text-shadow: 0 1px rgba(255, 255, 255, .75);
-	cursor: pointer;
-	margin-bottom: 20px;
-	line-height: normal;
-	padding: 8px 10px;
-	font-family: "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
}
...
```

Now, we're ready to add our own. We're going to round off the corners of our submit buttons first. The properties with `background-clip` will ensure the color stops at the border, preventing it from bleeding past that point. We've adjusted the background color to our blue and our font color to white.

```CSS(stylesheets/base.css)
...
input[type="submit"],
input[type="reset"],
input[type="button"] {
+	-moz-border-radius: 8px;
+	-webkit-border-radius: 8px;
+	border-radius: 8px; /* border radius */
+	-moz-background-clip: padding;
+	-webkit-background-clip: padding-box;
+	background-clip: padding-box; /* prevents bg color from leaking outside the border */
+	background-color: #009ae8; /* layer fill content */
+	color: #fff;
+	font-size: 1.2em;
+	border:0;
+	text-transform: uppercase;
+	font-weight: 900;
+	padding:0.82em 2.5em;
+	cursor: pointer;
+	margin:0;
}
...
```

After a bit of trial and error, we've adjusted the padding within our buttons to give it the proper spacing. Because it's an input, it will come with pre-existing styles defaulted from the browser you're using. One of these include a nasty looking border. So we can adjust and fix this by giving `border` a value of `0`.

Next, we are going to update how our button looks when the user hovers over it. Before, Skeleton provided a simple gradient button with a gradient color change on hover. Since we're going fairly flat with this design, we're going to remove all the unnecessary styles, and just add a varying shade of our blue as the background color.

```CSS(stylesheets/base.css)
...
input[type="submit"],
input[type="reset"],
input[type="button"] {
	-moz-border-radius: 8px;
	-webkit-border-radius: 8px;
	border-radius: 8px; /* border radius */
	-moz-background-clip: padding;
	-webkit-background-clip: padding-box;
	background-clip: padding-box; /* prevents bg color from leaking outside the border */
	background-color: #009ae8; /* layer fill content */
	color: #fff;
	font-size: 1.2em;
	border:0;
	text-transform: uppercase;
	font-weight: 900;
	padding:0.82em 2.5em;
	cursor: pointer;
	margin:0;
}
.button:hover,
button:hover,
input[type="submit"]:hover,
input[type="reset"]:hover,
input[type="button"]:hover {
-	color: #222;
-	background: #ddd; /* Old browsers */
-	background: #ddd -moz-linear-gradient(top, rgba(255,255,255,.3) 0%, rgba(0,0,0,.3) 100%); /* FF3.6+ */
-	background: #ddd -webkit-gradient(linear, left top, left bottom, color-stop(0%,rgba(255,255,255,.3)), color-stop(100%,rgba(0,0,0,.3))); /* Chrome,Safari4+ */
-	background: #ddd -webkit-linear-gradient(top, rgba(255,255,255,.3) 0%,rgba(0,0,0,.3) 100%); /* Chrome10+,Safari5.1+ */
-	background: #ddd -o-linear-gradient(top, rgba(255,255,255,.3) 0%,rgba(0,0,0,.3) 100%); /* Opera11.10+ */
-	background: #ddd -ms-linear-gradient(top, rgba(255,255,255,.3) 0%,rgba(0,0,0,.3) 100%); /* IE10+ */
-	background: #ddd linear-gradient(top, rgba(255,255,255,.3) 0%,rgba(0,0,0,.3) 100%); /* W3C */
-	border: 1px solid #888;
-	border-top: 1px solid #aaa;
-	border-left: 1px solid #aaa;
+	background:#0483c3; 
}
```

For this particular case, we're going to eliminate all the styles under the active state of our button. You could add in the same background color as the hover if you like, but for now, let's just remove all below our active state.

```CSS(stylesheets/base.css)
...
input[type="submit"],
input[type="reset"],
input[type="button"] {
	-moz-border-radius: 8px;
	-webkit-border-radius: 8px;
	border-radius: 8px; /* border radius */
	-moz-background-clip: padding;
	-webkit-background-clip: padding-box;
	background-clip: padding-box; /* prevents bg color from leaking outside the border */
	background-color: #009ae8; /* layer fill content */
	color: #fff;
	font-size: 1.2em;
	border:0;
	text-transform: uppercase;
	font-weight: 900;
	padding:0.82em 2.5em;
	cursor: pointer;
	margin:0;
}
.button:hover,
button:hover,
input[type="submit"]:hover,
input[type="reset"]:hover,
input[type="button"]:hover {
	background:#0483c3; 
}
.button:active,
button:active,
input[type="submit"]:active,
input[type="reset"]:active,
input[type="button"]:active {
-	border: 1px solid #666;
-	background: #ccc; /* Old browsers */
-	background: #ccc -moz-linear-gradient(top, rgba(255,255,255,.35) 0%, rgba(10,10,10,.4) 100%); /* FF3.6+ */
-	background: #ccc -webkit-gradient(linear, left top, left bottom, color-stop(0%,rgba(255,255,255,.35)), color-stop(100%,rgba(10,10,10,.4))); /* Chrome,Safari4+ */
-	background: #ccc -webkit-linear-gradient(top, rgba(255,255,255,.35) 0%,rgba(10,10,10,.4) 100%); /* Chrome10+,Safari5.1+ */
-	background: #ccc -o-linear-gradient(top, rgba(255,255,255,.35) 0%,rgba(10,10,10,.4) 100%); /* Opera11.10+ */
-	background: #ccc -ms-linear-gradient(top, rgba(255,255,255,.35) 0%,rgba(10,10,10,.4) 100%); /* IE10+ */
-	background: #ccc linear-gradient(top, rgba(255,255,255,.35) 0%,rgba(10,10,10,.4) 100%); /* W3C */
}
```

For the last part of the inputs and buttons, we are going to update a few things to our text field. To match our button, we're going to round the corners a bit more, changing it from two pixels to 8 pixels. We also need to add in our new font choice, 'Lato', that we've used throughout the page.

```css(stylesheet/base.css)
...
input[type="submit"],
input[type="reset"],
input[type="button"] {
	-moz-border-radius: 8px;
	-webkit-border-radius: 8px;
	border-radius: 8px; /* border radius */
	-moz-background-clip: padding;
	-webkit-background-clip: padding-box;
	background-clip: padding-box; /* prevents bg color from leaking outside the border */
	background-color: #009ae8; /* layer fill content */
	color: #fff;
	font-size: 1.2em;
	border:0;
	text-transform: uppercase;
	font-weight: 900;
	padding:0.82em 2.5em;
	cursor: pointer;
	margin:0;
}
.button:hover,
button:hover,
input[type="submit"]:hover,
input[type="reset"]:hover,
input[type="button"]:hover {
	background:#0483c3; 
}
.button:active,
button:active,
input[type="submit"]:active,
input[type="reset"]:active,
input[type="button"]:active { }
...
input[type="text"],
input[type="password"],
input[type="email"],
textarea,
select {
	border: 1px solid #ccc;
-	padding: 6px 4px;
+	padding: 0.75em 1em;
	outline: none;
-	-moz-border-radius: 2px;
-	-webkit-border-radius: 2px;
-	border-radius: 2px;
-	font: 13px "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
+	-moz-border-radius: 8px;
+	-webkit-border-radius: 8px;
+	border-radius: 8px;
+	font: 1.2em "Lato", "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
	color: #777;
	margin: 0;
-	width: 210px;
+	width: 90%;
	max-width: 100%;
	display: block;
	margin-bottom: 20px;
}
...
```

Before, Skeleton had a set width to their input fields. We've removed the set pixel width, and applied a percentage width. We've opted for 90% for it to fit the width of the columns its residing in. We've also updated the padding so that it will be similar in height to that of the button.

Now that our header is finally complete, we can move onto the next section of our page: Benefits.
  
### Benefits

![](http://cl.ly/WHK4/13-benefits.png)

Now, navigate to the bottom of your `base.css` file after the `header` section styles. Begin a new comment for our Benefits section of the page.

The first task is to update the padding at the top of this section, to provide some additional spacing between the bottom of the header image. Whitespace provides the eye with some relief as the user moves down the page, and also gives each element to breathe.

```css(stylesheets/base.css)
...
+/* Benefits */
+#benefits {
+	padding:4em 0 0;
+	text-align: center;
+}
```

We've also set the alignment of the text to be centered. This will allow our header, paragraph text and image to move to the center horizontally on the page.

Next, we're going to change the color and font weight of our header.

```css(stylesheets/base.css)
...
/* Benefits */
#benefits {
	padding:4em 0 0;
	text-align: center;
}
+#benefits h2 {
+	color:#009be8;
+	font-weight: 300;
+}
```

We're reusing the blue for this header color and made the font slightly thinner. Now we can style the paragraph text. We'll reuse these styles later on for another section.

```css(stylesheets/base.css)
...
/* Benefits */
#benefits {
	padding:4em 0 0;
	text-align: center;
}
#benefits h2 {
	color:#009be8;
	font-weight: 300;
}
+#benefits p {
+	color:#9d9d9d;
+	font-size:1.2em;
}
```

We've increased the text size to `1.2em` and changed the color. This will help make it more readable and play well with the rest of the page.

Next, we're going to style the pricing section, which is the more complex of the sections on our page.