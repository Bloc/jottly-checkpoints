## Using Blockquotes for Testimonials

![Testimonials](http://cl.ly/WGoP/05-testimonials.png)

In this checkpoint we'll create a Testimonials section and add three blockquotes to it. Testimonials should help prospective customers with their decision to buy a product.

Let's give this div an id named testimonials and place it below the pricing section:

```html(index.html)
+ <!-- Testimonials
+ ================================================== -->
+ <div id="testimonials">
+ </div>
```

Next, we'll create a header using an h2 tag and a paragraph tag to display the explanation:

```html(index.html)
<!-- Testimonials
================================================== -->
<div id="testimonials">
+ <h2>Who's using it?</h2>
+ <p>Jott.ly has around 150,000 satisfied customers sharing and collaborating with teams throughout 35 countries. Here’s what a few had to say:</p>
</div>
```

Let's create our first blockquote. A blockquote is an HTML element that contains quoted text.

```html(index.html)
<!-- Testimonials
================================================== -->
<div id="testimonials">
  <h2>Who's using it?</h2>
  <p>Jott.ly has around 150,000 satisfied customers sharing and collaborating with teams throughout 35 countries. Here’s what a few had to say:</p>
+
+ <blockquote>
+   “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo."
+ </blockquote>
</div>
```

Next, we'll add a new div to hold the image of the customer and their name:

```html(index.html)
<!-- Testimonials
================================================== -->
<div id="testimonials">
  <h2>Who's using it?</h2>
  <p>Jott.ly has around 150,000 satisfied customers sharing and collaborating with teams throughout 35 countries. Here’s what a few had to say:</p>

  <blockquote>
    “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo."
  </blockquote>
+ <div class="avatar">
+   <img src="images/avatar1.jpg" />
+   <p>Danny S.</p>
+ </div>
</div>
```

Because we'll use a similar structure and styling for all three blockquotes, we created a div and gave it a class of avatar.

Create the other two blockquotes:

```html(index.html)
<!-- Testimonials
================================================== -->
<div id="testimonials">
  <h2>Who's using it?</h2>
  <p>Jott.ly has around 150,000 satisfied customers sharing and collaborating with teams throughout 35 countries. Here’s what a few had to say:</p>

  <blockquote>
    “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo."
  </blockquote>
  <div class="avatar">
    <img src="images/avatar1.jpg" alt="Danny S." />
    <p>Danny S.</p>
  </div>
+
+ <blockquote>
+   “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo."
+ </blockquote>
+ <div class="avatar">
+   <img src="images/avatar2.jpg" alt="Jonathan M."  />
+   <p>Jonathan M.</p>
+ </div>
+  
+ <blockquote>
+   “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo."
+ </blockquote>
+ <div class="avatar">
+   <img src="images/avatar3.jpg" alt="Chloe P."  />
+   <p>Chloe P.</p>
+ </div>
+
</div>
```

Refresh your browser to viewthe changes.

### Github

Push your changes to Github:

```bash(Terminal)
$ git add .
$ git commit -m "Added blockquote testimonials"
$ git push origin gh-pages
```

In the next checkpoint we'll create an email input field and a footer to complete our landing page structure.
