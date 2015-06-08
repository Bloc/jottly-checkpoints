## Adding an Email Input and Footer

<center>![Finishing HTML](https://bloc-global-assets.s3.amazonaws.com/images-design/blocbooks/jottly/jottlyfooter.png)</center>

In this checkpoint we'll add the last two sections to our landing page. The first section will have an email input field and a submit button. The second section  will contain the footer where we'll provide additional links and content, such as copyright text.

### Call to action

Near the bottom of the page, we'll add a "call-to-action". A call-to-action should provide users with an obvious action for getting more information or buying a product. In our case, we want users to be able to sign up for Jottly.

Like the other sections, we'll add a comment to denote where the call-to-action section begins. We'll give this div an id named "action":

```html(index.html)
+ <!-- Call to Action
+ ================================================== -->
+ <section class="action">
+   <h2>Give it a try before you commit.</h2>
+   <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
+ </section>
```

Add an input field and button:

```html(index.html)
<!-- Call to Action
================================================== -->
<section class="action">
  <h2>Give it a try before you commit.</h2>
  <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
+
+ <input type="email" placeholder="Enter your e-mail address"/>
+ <button type="submit">Sign Up Now!</button>
</section>
```

### Footer

Let's create the footer section:

```html(index.html)
...
  </section
</main>
+
+ <!-- Footer
+ ================================================== -->
+ <footer>
+ </footer>
```

On the left side of the footer, we'll include navigation links. Be sure to wrap the text inside the list item tags with anchor tags. Anchor tags tells the browser that these will be links, even if we're not linking to anything yet.

```html(index.html)
...
<!-- Footer
================================================== -->
<footer>
+ <nav>
+   <ul>
+     <li><a href="#">About</a></li>
+     <li><a href="#">Contact</a></li>
+     <li><a href="#">Privacy Policy</a></li>
+     <li><a href="#">Terms</a></li>
+   </ul>
+ </nav>
</footer>
```

The last two items we'll add to the footer are a smaller logo and the copyright text. This will help reinforce our brand and provide the basic copyright information to all visitors.

```html(index.html)
<!-- Call to Action
================================================== -->
<div id="action">
  <h2>Give it a try before you commit.</h2>
  <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>

  <input type="text" placeholder="Enter your email address"/>
  <button type="submit">Sign Up Now!</button>
</div>

<!-- Footer
================================================== -->
<footer>
  <nav>
    <ul>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
      <li><a href="#">Privacy Policy</a></li>
      <li><a href="#">Terms</a></li>
    </ul>
  </nav>
+ <img src="images/small_logo.png" />
+ <p>&copy; 2015. Jott.ly. All Rights Reserved.</p>
</footer>
```

Refresh your browser to see the changes. We've completed the basic HTML structure for our landing page! Now we can focus on formatting our page with Skeleton's grid layout.