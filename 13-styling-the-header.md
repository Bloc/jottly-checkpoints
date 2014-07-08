## Styling the Header

![](http://cl.ly/WHHY/12-style-header.png)

In this checkpoint we'll update the navigation style, the header text and the email input form.

### Navigation

First, we'll add a simple class to the second list item link in our navigation area. This class will make the link look like a button:

```html(index.html)
<nav>
  <ul>
    <li><a href="#">Sign In</a></li>
-   <li><a href="#">Sign Up Now!</a></li>
+   <li><a class="btn" href="#">Sign Up Now!</a></li>
  </ul>
</nav>
```

We'll add a style for the btn class in our CSS file, but before we do we'll move the nav area to the right side of the page. We'll add the text-align property to our header nav and give it a value of "right". We'll also add a small margin to the top of the navigation area to push it down a bit so it's not being cut off by the browser window. Remember that this new code should be added at the bottom of the base.css file.

```css(stylesheets/base.css)
+#header nav {
+ text-align:right;
+ margin-top:2em;
+}
+#header nav ul li {
+ display:inline-block;
+}
```

### Display

HTML elements are naturally displayed as boxes on within a browser. You can change how these line up with the display property.

![](https://bloc-global-assets.s3.amazonaws.com/images-design/jottly/css/css-display.png)

If you want your elements to display next to each other horizontally, you can apply the inline value. This is something you'll use when creating navigational elements to place in a horizontal pattern. Inline elements also retain no whitespace above or below, whereas block elements do. If using inline, remember that items will not automatically create a new line, but just continue as one stream of elements.

"Block" adds space above and below, and creates an entirely new line for each element, forcing the next one to fall on the line below.

"Inline-block" is a hybrid of both inline and block. This value provides space above and below each element, while aligning them on a single line.

Let's get back to adjusting the navigation links. We'll adjust the padding, color and text qualities of the links to match our product mockup.

```css(stylesheets/base.css)
#header nav {
  text-align:right;
  margin-top:2em;
}
#header nav ul li {
  display:inline-block;
}
+#header nav ul li a {
+ color:#fff;
+ text-transform:uppercase;
+ text-decoration:none;
+ padding:0.75em 2em;
+}
```

To change the color of the text, we targeted the anchor tag within the list items, and set the color to white, which is #fff in [hexidecimal format](http://www.w3schools.com/tags/ref_colorpicker.asp). We removed the link underline by giving the text-decoration property a value of "none".

Let's style our button:

```css(stylesheets/base.css)
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
+ -moz-border-radius: 8px;
+ -webkit-border-radius: 8px;
+ border-radius: 8px; /* border radius */
+ border:2px solid #fff;
+}
+#header nav ul li a.btn:hover {
+ background:#fff;
+ color:#009be8;
+}
```

The rounded box around the text uses the "border-radius" property, which creates a nice-looking button.

border-radius vendor prefixes are used for multiple types of browser support. For example, some CSS properties render differently in different browsers if a vender prefix is not specified. "-moz" targets Mozilla's Firefox, and  "-webkit" targets Chrome and Safari.

### Text

Let's fix the text on top of the header image. Before we style it, let's add a new class to the nine column element in index.html:

```html(index.html)
<div class="container">
-  <div class="nine columns">
+  <div class="nine columns headertext">
     <h1>An easier way to write &amp; collaborate</h1>
     <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
```

Within base.css, we will add the selectors to target each element and begin styling the text. We'll start by moving the entire box down the page a bit, so it has some breathing room:

```css(stylesheets/base.css)
+#header .headertext {
+ margin-top: 10em;
+}
```

Next, we'll change the color, font weight, size and other properties of h1 elements:

```css(stylesheets/base.css)
#header .headertext {
  margin-top: 10em;
}
+#header h1 {
+ color:#fff;
+ font-weight:300;
+ font-size:4.5em;
+ line-height: 1;
+ text-shadow: 0 1px 2px rgba(0,0,0,.2);
+ margin-bottom: 0.3em;
+}
```

We have increased the size to 4.5em, which scales the text to fit nicely in our columns. The line-height property determines the spacing between lines. The value of 1 keeps the lines tight without overlapping. We also added a text shadow to help the text pop off the background and provide some depth.

The text shadow property is broken down by the following values:

```css
text-shadow { horizontal vertical blur color}
```

The values above set the horizontal shadow to 0, vertical to 1 and blur to 2. We set the color in RGBA, which gives us the ability to add some transparency or opacity to the color. 0,0,0 in RGB represents black, and we've made 20% opaque.

Next, we'll update the properties of the paragraph text below the h1:

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
+ color:#d5d5d5;
+ font-size:1.33em;
+ line-height: 1.5;
+ text-shadow: 0 1px 2px rgba(0,0,0,.2);
+ margin-bottom: 1.2em;
+}
+#header p strong {
+ color:#fff;
+}
```

We updated the font color to be light gray. We updated the font size to be slightly larger than the normal size. The line-height has been set to be 1.5 to allow for easier readability between the lines of text in this block. Again, we've added a slight text shadow, and set a margin below this element for pleasant spacing.

Because we have a strong tag inside our paragraph tag, we are able to emphasize key words we want customers to focus on.

Next we'll improve the email input form and the benefits section of our site.
