## Finishing the HTML for email input and footer

![Finishing HTML](http://cl.ly/WH7j/06-html-finishes.png)

In this checkpoint we'll add the last two sections to our landing page. The first section will have an email input field and a submit button. The second section  will contain the footer, where we'll provide additional links and content, such as copyright text.

### Call to action

Near the bottom of the page, we'll want a "Call to Action". A call to action should provide users with an obvious action for getting more information or buying a product. In our case, we want users to be able to sign up for Jottly.

Like the other sections, we'll add a comment to denote where the Call to Action section begins. We'll give this div an id named action:

```html(index.html)
+ <!-- Call to Action
+ ================================================== -->
+ <div id="action">
+   <h2>Give it a try before you commit.</h2>
+   <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
+ </div>
```

Add an input field and button to complete the call to action:

```html(index.html)
<!-- Call to Action
================================================== -->
<div id="action">
  <h2>Give it a try before you commit.</h2>
  <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
+
+ <input type="text" placeholder="Enter your email address"/>
+ <button type="submit">Sign Up Now!</button>
</div>
```

### Footer

Let's create the footer section:

```html(index.html)
<!-- Call to Action
================================================== -->
<div id="action">
  <h2>Give it a try before you commit.</h2>
  <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>

  <input type="text" placeholder="Enter your email address"/>
  <button type="submit">Sign Up Now!</button>
</div>
+
+ <!-- Footer
+ ================================================== -->
+ <div id="footer">
+ </div>
```

On the left side of the footer, we'll include navigation links. Be sure to wrap the text inside the list item tags with anchor tags. Anchor tags tells the browser that these will be links, even if we're not linking to anything yet.

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
<div id="footer">
+ <nav>
+   <ul>
+     <li><a href="#">About</a></li>
+     <li><a href="#">Contact</a></li>
+     <li><a href="#">Privacy Policy</a></li>
+     <li><a href="#">Terms</a></li>
+   </ul>
+ </nav>
</div>
```

The last two items we'll add to the footer is a smaller logo and the copyright text. This will help reinforce our brand and provide the basic copyright information to all visitors.

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
<div id="footer">
  <nav>
    <ul>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
      <li><a href="#">Privacy Policy</a></li>
      <li><a href="#">Terms</a></li>
    </ul>
  </nav>
+ <img src="images/small_logo.png" />
+ <p>&copy; 2014. Jott.ly. All Rights Reserved.</p>
</div>
```

Refresh to see the changes. We've completed the basic HTML structure for our landing page! Now we can integrate a Skeleton grid layout and style our page. 

### Pushing your changes

Push your changes to Github:

```bash(Terminal)
$ git add .
$ git commit -m "Added a call to action and footer"
$ git push origin gh-pages
```
