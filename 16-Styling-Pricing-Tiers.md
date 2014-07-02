## Styling the Pricing Tiers

![](http://cl.ly/WHKa/14-pricing.png)

In this checkpoint we'll style the pricing section. We'll add some cool text formatting and make the Small Business plan stand out as the recommended tier.

### Base styles

Before we update the price divs, we need to modify the pricing section. We want to change the background to blue, but in order for the content to appear nicely, we also need to add padding. While we're at it, we'll adjust the color of the header and paragraph text:

```css(stylesheets/base.css)
+/* Pricing */
+#pricing {
+ background:#009be8;
+ padding:4em 0;
+ text-align: center;
+}
+#pricing h2 {
+ color:#fff;
+ font-weight:300;
+ text-shadow: 0 1px 2px rgba(0,0,0,.2);
+}
+#pricing p {
+ color:#fff;
+ text-shadow: 0 1px 2px rgba(0,0,0,.2);
+ font-size:1.2em;
+}
```

Notice that we added a text shadow to the h2 and p tags to help them pop off the page.

### Price Box

We created a pricebox div to frame our pricing content. Let's change the background color to white so it contrasts nicely with the blue background:

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
+ background-color: #fff;
+ -moz-box-shadow: 0 1px 3px rgba(0,0,0,.2);
+ -webkit-box-shadow: 0 1px 3px rgba(0,0,0,.2);
+ box-shadow: 0 1px 3px rgba(0,0,0,.2);
+ margin-top:3em;
+ height:400px;
+ position: relative;
+}
```

We added a box shadow to give the price boxes a layering effect. We used browser prefixes to ensure this styling appears consistently in Mozilla, Chrome, Safari and other modern browsers. Much like the text shadow, the box shadow syntax can be broken down into pieces:

```css
box-shadow: horizontal vertical blur color;
```

We also changed the height of the box, which is something we'll use in the next step. The relative position property will come in handy for positioning other elements around the pricing divs.

### Differentiating Price Boxes

For our second box — Small Businesses — we'll add a second class named "deal" to the pricebox div. This will differentiate the middle box from the other two, and represent our recommended "best deal" for customers.

```html(index.html)
 ...
    <div class="one-third column">
-     <div class="pricebox">
+       <div class="pricebox deal">
         <header>
           <h3>Small Businesses</h3>
         </header>
         <section>
...
```

Now we'll add a new class selector to our base.css file which targets the pricebox and deal classes. We've minimized the top margin so it stands taller than the other divs. We also adjusted the height so it extends down further as well.

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
+ margin-top:2em;
+ height:430px;
+}
```

### Header

Let's update the h3 header to change the background, add a small box shadow and adjust the padding:

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
+ background-color: #f1f1f1;
+ -moz-box-shadow: 0 1px 3px rgba(0,0,0,.2);
+ -webkit-box-shadow: 0 1px 3px rgba(0,0,0,.2);
+ box-shadow: 0 1px 3px rgba(0,0,0,.2);
+ padding:1em 0;
+ margin-bottom:2em;
+}
+.pricebox header h3 {
+ color:#4d4d4d;
+ font-size:1.4em;
+ text-transform: uppercase;
+ margin:0;
+ font-weight: 600;
+}
```

We changed up the h3 text styles to be uppercase and heavier. We increased the size to make the header more prominent.

### Buttons

Let's change the button color to a shade of green. We want to position it to always be at the bottom of the price box, spaced 1em from the bottom edge, no matter what the height of the box is. This will align the two outer buttons and will keep the spacing consistent in the middle box as well.

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
+ background:#2ecc71;
+ position:absolute;
+ bottom:1em;
+ width:90%;
+ left:0;
+ right:0;
+ margin:0 auto;
+ text-align: center;
+}
+.pricebox section button:hover {
+ background:#1fae5c;
+}
```

We set the width to 90% of the button so it doesn't hit the outer edges of the box. And adding a margin of 0 auto which will center the element inside the box.

### Price Text

For the pricing of our services, we want to increase the text size to give it prominence over the rest of the content inside each of the boxes:

```css(stylesheets/base.css)
...
+.pricebox section h4 {
+ display:inline-block;
+ color:#009be8;
+ font-size: 6em;
+ font-weight: 900;
+ vertical-align: bottom;
+}
```

We changed the color and size of the pricing font. Before we go further, we need to update our HTML so we can use this style. We'll add a span around the dollar symbol, and then provide a break between "per month" and "per user" so they appear on two lines:

```html(index.html)
...
          <h3>Individuals &amp; Family</h3>
        </header>
        <section>
-       <h4>$2</h4>
-       <p>per month/per user</p>
+       <h4><span>$</span>2</h4>
+       <p>per month<br/>/per user</p>
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
-       <h4>$5</h4>
-       <p>per month/per user</p>
+       <h4><span>$</span>5</h4>
+       <p>per month<br/>/per user</p>
        <ul>
          <li>Unlimited notes</li>
          <li>Unlimited members</li>
...
          <h3>Enterprise</h3>
        </header>
        <section>
-       <h4>$8</h4>
-       <p>per month/per user</p>
+       <h4><span>$</span>8</h4>
+       <p>per month<br/>/per user</p>
        <ul>
          <li>Unlimited notes</li>
          <li>Unlimited members</li>
...
```

With our primary h4 size being 6em, we want to adjust the span inside of it to be half of that. If you enter 3em for the font size, you will see it massively larger than that of the price itself. This is because that number will multiply the number above it, meaning 6em x 3em = too big! We want to multiply it by 0.5em, so it gets smaller.

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
+ font-size:0.5em;
+ line-height: 1;
+ vertical-align: top;
+}
+#pricing .pricebox section p {
+ display:inline-block;
+ color:#9d9d9d;
+ text-shadow:none;
+ line-height: 1;
+ position:relative;
+ top:1em;
+ font-size:1.1em;
+}
```

Use your knowledge of CSS and explain each new property and value to yourself. You can add and remove properties and check out the results in your local browser to gain a better understand of their effect.

You can also right-click an element in your browser and select "Inspect Element". You can adjust CSS and HTML in real-time within Web Inspector. Any changes you make in Web Inspector will not be saved.

### List of Features

For our unordered features lists, we will add margin to the top so it doesn't interfere with the price area. For each list item, we'll slightly adjust the text size and provide some additional spacing in between each one so it's easier to read.

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
+ margin-top:3em;
+}
+.pricebox section ul li {
+ font-size:1.2em;
+ margin-bottom: 1.2em;
+}
```

### Pushing your changes

Push your changes to Github:

```bash(Terminal)
$ git add .
$ git commit -m "Styled pricing tiers"
$ git push origin gh-pages
```

Next we'll update the testimonials and action sections.
