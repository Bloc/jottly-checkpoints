## Improving the Testimonial, Call-to-Action and Footer Layouts

<center>![Testimonials Grid](https://bloc-global-assets.s3.amazonaws.com/images-design/blocbooks/jottly/jottlytestimonialsgrid.png)</center>

In this checkpoint we'll update the rest of our landing page with a grid layout.

### Testimonials

Much like the last section, we'll split the three testimonials into three columns across the page:

```html(index.html)
<!-- Testimonials
================================================== -->
<div id="testimonials">
+ <div class="container">
+   <div class="eight columns offset-by-two">
     <h2>Who's using it?</h2>
     <p>Jott.ly has around 150,000 satisfied customers sharing and collaborating with teams throughout 35 countries. Here’s what a few had to say:</p>
+   </div>
    <blockquote>
      “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
    </blockquote>
    <div class="avatar">
      <img src="images/avatar1.jpg" />
      <p>Danny S.</p>
    </div>
    <blockquote>
      “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
    </blockquote>
    <div class="avatar">
      <img src="images/avatar2.jpg" />
      <p>Jonathan M.</p>
    </div>
    <blockquote>
      “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
    </blockquote>
    <div class="avatar">
      <img src="images/avatar3.jpg" />
      <p>Chloe P.</p>
    </div>
+ </div>
</section>
```

Let's add the one-third column classes into a new div to space our testimonials evenly:

```html(index.html)
<!-- Testimonials
================================================== -->
<section class="testimonials">
  <div class="container">
    <div class="twelve columns offset-by-two">
      <h2>Who's using it?</h2>
      <p>Jott.ly has around 150,000 satisfied customers sharing and collaborating with teams throughout 35 countries. Here’s what a few had to say:</p>
    </div>
+   <div class="row">
+     <div class="one-third column">
        <blockquote>
         “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
        </blockquote>
        <div class="avatar">
          <img src="images/avatar1.jpg" />
          <p>Danny S.</p>
        </div>
+     </div>
+     <div class="one-third column">
        <blockquote>
          “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
        </blockquote>
        <div class="avatar">
          <img src="images/avatar2.jpg" />
          <p>Jonathan M.</p>
        </div>
+     </div>
+     <div class="one-third column">
        <blockquote>
          “Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
        </blockquote>
        <div class="avatar">
          <img src="images/avatar3.jpg" />
          <p>Chloe P.</p>
        </div>
+     </div>
+   </div>
  </div>
</section>
```

Refresh your browser to view your changes. You should have three columns, each with a quote, avatar image and the name of the person.

### Call-to-action

Let's apply the grid:

```html(index.html)
<!-- Call to Action
================================================== -->
    <section class="action">
+    <div class="container">
+      <div class="eight columns offset-by-two">
         <h2>Give it a try before you commit.</h2>
         <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
         <input type="email" placeholder="Enter your e-mail address"/>
         <button type="submit">Sign Up Now</button>  
+      </div>
+    </div>
    </section>
```

Let's create a separate section for our input and submit buttons:

```html(index.html)
<!-- Call to Action
================================================== -->
    <div id="action">
      <div class="container">
        <div class="twelve columns offset-by-two">
          <h2>Give it a try before you commit.</h2>
          <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
+         <div class="row">
+           <div class="eight columns alpha">
              <input type="email" placeholder="Enter your e-mail address"/>
+           </div>
+           <div class="four columns omega">
              <button type="submit">Sign Up Now</button>
+           </div>
+         </div>
        </div>
      </div>
    </div>
 ```

We wrapped the input field in an eight-column div with an alpha class so that it removes the padding and margins from the left side.

We also wrapped the button in a four-column div with an omega class. This aligns the input field with the submit button.

### Footer

We'll divide the footer in three divs. The majority of the footer will hold our navigation links on the left side of the page. We'll also create divs for the small logo and copyright text.

```html(index.html)
<!-- Footer
================================================== -->
<footer>
+ <div class="container">
+   <div class="eight columns">
      <nav>
        <ul>
          <li><a href="#">About</a></li>
          <li><a href="#">Contact</a></li>
          <li><a href="#">Privacy Policy</a></li>
          <li><a href="#">Terms</a></li>
        </ul>
      </nav>
+   </div>
+
+   <div class="two columns">
-     <img src="images/small_logo.png" />
+     <img src="images/small_logo.png" alt="Jottly" />
+   </div>
+
+   <div class="two columns">
      <p>&copy; 2014. Jott.ly. All Rights Reserved.</p>
+   </div>
+ </div>
</footer>
```

Notice the small change to the logo image. We added an alt attribute with a value of Jottly. This provides text to be displayed by default when the image cannot be displayed.

Examine the entire landing page. It should look much more organized than before. Each section should be somewhat distinct, even without much styling. By integrating a grid layout, we've greatly improved our landing page and it is now ready to be styled.