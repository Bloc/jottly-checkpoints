## Finishing the HTML for email input and footer

![Finishing HTML](http://cl.ly/WH7j/06-html-finishes.png)

In this checkpoint, we'll add in the last two sections of content for our Jott.ly landing page. The first will include an email input field along with a submit button, repeating the content from the header above. The second is our footer, to provide some additional links and content, such as copyright text.

### Call to action

Near the bottom of the page, we've included a new section that we're going to refer to as the 'Call to Action'. Here, we are giving the user an additional chance to sign up for Jott.ly if they've glossed over the previous opportunities.

Like the other sections, we'll add a comment to denote where this one begins. We'll give this `div` an `id` of 'action', just as shorthand.

```html(index.html)
+	<!-- Call to Action
+	================================================== -->
+	<div id="action">
+		<h2>Give it a try before you commit.</h2>
+		<p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>				
+	</div>
```

Since we've done this before, we'll go ahead and add in our `h2` and paragraph text. 

Now, just after the ending `</p>` tag, we can add in the code we used above. Any time you're able to reuse code, it will help you save time. So copy and paste the `input` and `button` tags from your header here.

```html(index.html)
<!-- Call to Action
================================================== -->
<div id="action">
     <h2>Give it a try before you commit.</h2>
     <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
+		
+    <input type="text" placeholder="Enter your email address"/>
+    <button type="submit">Sign Up Now</button>
</div>
```

Now we have our basic content for the action section. 

### Footer

Let's work on fixing up the footer. We're going to add a comment to section it off, and then create a `div` with an `id` of 'footer'.

```html(index.html)
<!-- Call to Action
================================================== -->
<div id="action">
     <h2>Give it a try before you commit.</h2>
     <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
		
     <input type="text" placeholder="Enter your email address"/>
     <button type="submit">Sign Up Now</button>
</div>
+
+	<!-- Footer
+	================================================== -->
+	<div id="footer">
+	</div>
```

On the left side of our footer, we want to include a few navigation links. Like before, we're going to start off with a `nav` tag, inserting an unordered list (`ul`) with four list items (`li`). Be sure to wrap the text inside the `li` with an anchor tag (`a`), so the browser knows these will be links — even if we're not linking to anything.

```html(index.html)
<!-- Call to Action
================================================== -->
<div id="action">
     <h2>Give it a try before you commit.</h2>
     <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
		
     <input type="text" placeholder="Enter your email address"/>
     <button type="submit">Sign Up Now</button>
</div>

<!-- Footer
================================================== -->
<div id="footer">
+     <nav>
+          <ul>
+               <li><a href="#">About</a></li>
+               <li><a href="#">Contact</a></li>
+               <li><a href="#">Privacy Policy</a></li>
+               <li><a href="#">Terms</a></li>
+          </ul>
+     </nav>
</div>
```

The last two items we're going to add into the footer is a smaller logo and the copyright text. This will help reinforce the brand and provide the basic copyright information to all visitors.

```html(index.html)
<!-- Call to Action
================================================== -->
<div id="action">
     <h2>Give it a try before you commit.</h2>
     <p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
		
     <input type="text" placeholder="Enter your email address"/>
     <button type="submit">Sign Up Now</button>
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
+    <img src="images/small_logo.png" />
+    <p>&copy; 2014. Jott.ly. All Rights Reserved.</p>
</div>
```

We're using the `img` tag to bring in the small logo inside your `images` directory. Next, we added in a paragraph tag to display the copyright text. 

And now, we've completed the basic HTML of our landing page for Jott.ly! Next, we're going to look at how to integrate the grid from Skeleton and then move onto styling our content.
