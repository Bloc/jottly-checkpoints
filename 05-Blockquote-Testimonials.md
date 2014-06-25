## Using Blockquotes for Testimonials

![Testimonials](http://cl.ly/WGoP/05-testimonials.png)

In this checkpoint, we will add three blockquotes to a new section for Testimonials. People love hearing rave reviews of a product, and for owners, it helps them sell their products better.

Like with the other sections we've created, we're going to start off with a comment, and give this `div` and `id` of 'testimonials'.

```html(index.html)
+	<!-- Testimonials
+	================================================== -->
+	<div id="testimonials">
+	</div>
```

Next, we'll add in our header using an `h2`, because of consistency across all sections, and a paragraph tag to continue the explanation.

```html(index.html)
<!-- Testimonials
================================================== -->
<div id="testimonials">
+		<h2>Who's using it?</h2>
+		<p>Jott.ly has around 150,000 satisfied customers sharing and collaborating with teams throughout 35 countries. Here’s what a few had to say:</p>
</div>
```

Once we have our basic text included, we can begin setting up our first `blockquote`. A `blockquote` is a set of text that is called out and is typically used when quoting outside sources, such as customers.

```html(index.html)
<!-- Testimonials
================================================== -->
<div id="testimonials">
     <h2>Who's using it?</h2>
     <p>Jott.ly has around 150,000 satisfied customers sharing and collaborating with teams throughout 35 countries. Here’s what a few had to say:</p>
+
+     <blockquote>
+          “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
+     </blockquote>
</div>
```

We wrap the text inside of quotations just so they appear on the page. You can opt to leave these out, as they are not a necessity.

Next, we're going to add in a new `div` to include the image of the customer and their name.

```html(index.html)
<!-- Testimonials
================================================== -->
<div id="testimonials">
     <h2>Who's using it?</h2>
     <p>Jott.ly has around 150,000 satisfied customers sharing and collaborating with teams throughout 35 countries. Here’s what a few had to say:</p>

     <blockquote>
          “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
     </blockquote>
+     <div class="avatar">
+          <img src="images/avatar1.jpg" />
+          <p>Danny S.</p>
+     </div>
</div>
```

Because we'll be using this across three different blockquotes, we create a new `div` and give it a `class` of 'avatar'. Inside, we're going to include an image from your `images` folder called `avatar1.jpg`. Next, we'll add some paragraph text to hold the name of the customer, in this case 'Danny S.'. Be sure to close the `div`, and you're all set.

We want to include two additional blockquotes, so much like our last checkpoint, we're going to use copy and paste.

```html(index.html)
<!-- Testimonials
================================================== -->
<div id="testimonials">
     <h2>Who's using it?</h2>
     <p>Jott.ly has around 150,000 satisfied customers sharing and collaborating with teams throughout 35 countries. Here’s what a few had to say:</p>

     <blockquote>
          “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
     </blockquote>
     <div class="avatar">
          <img src="images/avatar1.jpg" />
          <p>Danny S.</p>
     </div>
+
+    <blockquote>
+        “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
+    </blockquote>
+    <div class="avatar">
+        <img src="images/avatar2.jpg" />
+        <p>Jonathan M.</p>
+    </div>
+  
+    <blockquote>
+        “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
+    </blockquote>
+    <div class="avatar">
+        <img src="images/avatar3.jpg" />
+        <p>Chloe P.</p>
+    </div>
+
</div>
```

Copy from the opening `blockquote` tag up to the closing `</div>` for the avatar. Paste it twice below. Once you complete this, you can change out the images and the names for each of the customers. We're using Lorem ipsum filler text for the testimonials just to display the content.

Next, we're going to focus on the last few pieces of our landing page: the bottom email input and footer.
