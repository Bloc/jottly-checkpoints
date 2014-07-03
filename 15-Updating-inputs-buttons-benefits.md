## Updating Styles for the input field, buttons and Benefits

![Input and Button](http://cl.ly/WHKo/13-input.png)

In this checkpoint we'll create new styles for our input forms and the Benefits section.

### Input fields and buttons

Skeleton provides styles for inputs and buttons. We need to remove these so we can style ours the way we want. We'll need to locate the submit input styles in the base.css file, and remove the default properties and values:

```CSS(stylesheets/base.css)
...
input[type="submit"],
input[type="reset"],
input[type="button"] {
- background: #eee; /* Old browsers */
- background: #eee -moz-linear-gradient(top, rgba(255,255,255,.2) 0%, rgba(0,0,0,.2) 100%); /* FF3.6+ */
- background: #eee -webkit-gradient(linear, left top, left bottom, color-stop(0%,rgba(255,255,255,.2)), color-stop(100%,rgba(0,0,0,.2))); /* Chrome,Safari4+ */
- background: #eee -webkit-linear-gradient(top, rgba(255,255,255,.2) 0%,rgba(0,0,0,.2) 100%); /* Chrome10+,Safari5.1+ */
- background: #eee -o-linear-gradient(top, rgba(255,255,255,.2) 0%,rgba(0,0,0,.2) 100%); /* Opera11.10+ */
- background: #eee -ms-linear-gradient(top, rgba(255,255,255,.2) 0%,rgba(0,0,0,.2) 100%); /* IE10+ */
- background: #eee linear-gradient(top, rgba(255,255,255,.2) 0%,rgba(0,0,0,.2) 100%); /* W3C */
- border: 1px solid #aaa;
- border-top: 1px solid #ccc;
- border-left: 1px solid #ccc;
- -moz-border-radius: 3px;
- -webkit-border-radius: 3px;
- border-radius: 3px;
- color: #444;
- display: inline-block;
- font-size: 11px;
- font-weight: bold;
- text-decoration: none;
- text-shadow: 0 1px rgba(255, 255, 255, .75);
- cursor: pointer;
- margin-bottom: 20px;
- line-height: normal;
- padding: 8px 10px;
- font-family: "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
}
...
```

Now, we can add our own. We'll round off the corners of our submit buttons first. The properties with background-clip will ensure the color stops at the border, preventing it from bleeding past that point. We'll change the background color to blue and the font color to white:

```CSS(stylesheets/base.css)
...
input[type="submit"],
input[type="reset"],
input[type="button"] {
+ -moz-border-radius: 8px;
+ -webkit-border-radius: 8px;
+ border-radius: 8px; /* border radius */
+ -moz-background-clip: padding;
+ -webkit-background-clip: padding-box;
+ background-clip: padding-box; /* prevents bg color from leaking outside the border */
+ background-color: #009ae8; /* layer fill content */
+ color: #fff;
+ font-size: 1.2em;
+ border:0;
+ text-transform: uppercase;
+ font-weight: 900;
+ padding:0.82em 2.5em;
+ cursor: pointer;
+ margin:0;
}
...
```

We adjusted the padding within our buttons to give them the sufficient spacing. Buttons have a default style provided by the browser. One of these styles is a nasty-looking border. We adjusted the border by giving it a value of 0.

Next, we'll update how our button looks when a user hovers over it. By default, Skeleton provides a simple gradient button with a gradient color change on hover. Since we're implementing a flat design, we'll remove all the unnecessary styles, and just add a varied shade of blue as our button color:

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
- color: #222;
- background: #ddd; /* Old browsers */
- background: #ddd -moz-linear-gradient(top, rgba(255,255,255,.3) 0%, rgba(0,0,0,.3) 100%); /* FF3.6+ */
- background: #ddd -webkit-gradient(linear, left top, left bottom, color-stop(0%,rgba(255,255,255,.3)), color-stop(100%,rgba(0,0,0,.3))); /* Chrome,Safari4+ */
- background: #ddd -webkit-linear-gradient(top, rgba(255,255,255,.3) 0%,rgba(0,0,0,.3) 100%); /* Chrome10+,Safari5.1+ */
- background: #ddd -o-linear-gradient(top, rgba(255,255,255,.3) 0%,rgba(0,0,0,.3) 100%); /* Opera11.10+ */
- background: #ddd -ms-linear-gradient(top, rgba(255,255,255,.3) 0%,rgba(0,0,0,.3) 100%); /* IE10+ */
- background: #ddd linear-gradient(top, rgba(255,255,255,.3) 0%,rgba(0,0,0,.3) 100%); /* W3C */
- border: 1px solid #888;
- border-top: 1px solid #aaa;
- border-left: 1px solid #aaa;
+ background:#0483c3;
}
```

We'll eliminate all the styles for the active state of our button. We could add the same background color as the hover, but first let's just remove all styling for the active state:

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
- border: 1px solid #666;
- background: #ccc; /* Old browsers */
- background: #ccc -moz-linear-gradient(top, rgba(255,255,255,.35) 0%, rgba(10,10,10,.4) 100%); /* FF3.6+ */
- background: #ccc -webkit-gradient(linear, left top, left bottom, color-stop(0%,rgba(255,255,255,.35)), color-stop(100%,rgba(10,10,10,.4))); /* Chrome,Safari4+ */
- background: #ccc -webkit-linear-gradient(top, rgba(255,255,255,.35) 0%,rgba(10,10,10,.4) 100%); /* Chrome10+,Safari5.1+ */
- background: #ccc -o-linear-gradient(top, rgba(255,255,255,.35) 0%,rgba(10,10,10,.4) 100%); /* Opera11.10+ */
- background: #ccc -ms-linear-gradient(top, rgba(255,255,255,.35) 0%,rgba(10,10,10,.4) 100%); /* IE10+ */
- background: #ccc linear-gradient(top, rgba(255,255,255,.35) 0%,rgba(10,10,10,.4) 100%); /* W3C */
}
```

To match our button style, we'll round the corners of our text input. We'll also add our new font choice - Lato.

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
- padding: 6px 4px;
+ padding: 0.75em 1em;
  outline: none;
- -moz-border-radius: 2px;
- -webkit-border-radius: 2px;
- border-radius: 2px;
- font: 13px "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
+ -moz-border-radius: 8px;
+ -webkit-border-radius: 8px;
+ border-radius: 8px;
+ font: 1.2em "Lato", "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
  color: #777;
  margin: 0;
- width: 210px;
+ width: 90%;
  max-width: 100%;
  display: block;
  margin-bottom: 20px;
}
...
```

Skeleton provides a default width to their input fields. We removed the default width and applied a custom percentage width. We opted for 90% to fill most of column it's residing in. We also updated the padding so that it will be similar in height to that of the button.

Now that our header is complete, we can move onto the Benefits section.

### Benefits

![](http://cl.ly/WHK4/13-benefits.png)

Navigate to the bottom of the base.css file after the header section styles.

The first task is to update the padding at the top of this section to provide additional spacing at the bottom of the header image. Whitespace gives the eye with some relief as the user reads down the page, and also gives each element room to breathe.

```css(stylesheets/base.css)
...
+/* Benefits */
+#benefits {
+ padding:4em 0 0;
+ text-align: center;
+}
```

We set the alignment of the text to be centered. This will allow our header, paragraph text and image to be centered horizontally.

Next, we'll change the color and font weight of our header:

```css(stylesheets/base.css)
...
/* Benefits */
#benefits {
  padding:4em 0 0;
  text-align: center;
}
+#benefits h2 {
+ color:#009be8;
+ font-weight: 300;
+}
```

We reused the blue for this header color and made the font slightly thinner. Now we can style the paragraph text. We'll reuse these styles later for another section.

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
+ color:#9d9d9d;
+ font-size:1.2em;
}
```

We increased the text size to 1.2em and changed the color. This will improve readability and look nice with the rest of the page.

### Pushing your changes

Push your changes to Github:

```bash(Terminal)
$ git add .
$ git commit -m "Styled input forms and the benefits section"
$ git push origin gh-pages
```

Next, we'll style the pricing section, which is the most complex section on our landing page.
