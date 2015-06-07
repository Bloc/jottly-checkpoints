## Styling Components and the Benefits Section

<center>![Input and Button](https://bloc-global-assets.s3.amazonaws.com/images-design/blocbooks/jottly/jottlyinputs.png)</center>

In this checkpoint we'll style our input and button components, as well as the Benefits section.

### Inputs and buttons

Skeleton provides default styles for inputs and buttons. We need to adjust these defaults so we can apply our own custom styles. We'll need to locate the input styles in `skeleton.css`, and customize:

```css(css/skeleton.css)
.button,
button,
input[type="submit"],
input[type="reset"],
input[type="button"] {
  display: inline-block;
  height: 38px;
  padding: 0 30px;
- color: #555;
+ color: #fff;
+ background-color: #009AE8;
  text-align: center;
- font-size: 11px;
+ font-size:1em;
  font-weight: 600;
  line-height: 38px;
  letter-spacing: .1rem;
  text-transform: uppercase;
  text-decoration: none;
  white-space: nowrap;
- background-color: transparent;
  border-radius: 4px;
- border: 1px solid #bbb;
+ border: none;
  cursor: pointer;
  box-sizing: border-box;
+ -moz-background-clip: padding;
+ -webkit-background-clip: padding-box;
+ background-clip: padding-box; /* prevents bg color from leaking outside the border */ }
```

The properties with "background-clip" will ensure the color stops at the border, preventing it from bleeding past. We changed the background color to blue and the font color to white.

Next, we'll update how our button looks when a user hovers over it. By default, Skeleton provides a text color change on hover:

```css(css/skeleton.css)
.button:hover,
button:hover,
input[type="submit"]:hover,
input[type="reset"]:hover,
input[type="button"]:hover,
.button:focus,
button:focus,
input[type="submit"]:focus,
input[type="reset"]:focus,
input[type="button"]:focus {
- color: #333;
+ color: #fff;
- border-color: #888;
+ border-color:transparent;
+ background-color: #0483c3;
  outline: 0; }
```

We'll update the size of our input field to fill the column container:

```css(css/skeleton.css)
input[type="email"],
input[type="number"],
input[type="search"],
input[type="text"],
input[type="tel"],
input[type="url"],
input[type="password"],
textarea,
select {
  height: 38px;
  padding: 6px 10px; /* The 6px vertically centers text on FF, ignored by Webkit */
  background-color: #fff;
  border: 1px solid #D1D1D1;
  border-radius: 4px;
  box-shadow: none;
  box-sizing: border-box;
+ width:100%; }
```

Now that our header is complete, we can move onto the Benefits section.

### Benefits

<center>![Benefits Styles](https://bloc-global-assets.s3.amazonaws.com/images-design/blocbooks/jottly/jottlybenefitscss.png)</center>

Navigate to the bottom of `skeleton.css` after the header section styles. The first task is to update the padding at the top of this section to provide additional spacing at the bottom of the header image. Whitespace gives the eye with some relief as the user reads down the page, and also gives each element room to breathe.

```css(css/skeleton.css)
+/* Benefits */
+.benefits {
+ padding:4em 0 0;
+ text-align: center;
+}
```

We set the alignment of the text to be centered. This will allow our header, paragraph text and image to be centered horizontally.

Next, we'll change the color and font weight of our header:

```css(css/skeleton.css)
/* Benefits */
.benefits {
  padding:4em 0 0;
  text-align: center;
}
+.benefits h2 {
+ color:#009be8;
+ font-weight: 300;
+}
```

We reused the blue for this header color and made the font slightly thinner. Now we can style the paragraph text. We'll reuse these styles later in another section.

```css(css/skeleton.css)
/* Benefits */
.benefits {
  padding:4em 0 0;
  text-align: center;
}
.benefits h2 {
  color:#009be8;
  font-weight: 300;
}
+.benefits p {
+ color:#9d9d9d;
+ font-size:1.1em;
}
```

We changed the text size and color to improve readability and look nice with the rest of the page. We need to ensure our image fits within the container, so we'll add a few properties to make it responsive:

```css(css/skeleton.css)
...
+img {
+ max-width:100%;
+ height:auto;
+}
```

Next, we'll style the pricing section, which is the most complex section on our landing page.
