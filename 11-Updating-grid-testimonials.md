## Updating grids for Testimonials, Action and Footer

![](http://cl.ly/WHRe/10-testimonials.png)

In this checkpoint, we're going to finish integrating the Skeleton grid to the remainder of the page. We'll first tackle our testimonials, moving onto the action section and finally the footer.

### Testimonials

Much like the last section, we're going to split our three testimonials into three columns across the page. Before doing so, we can apply the same column widths to the header text and paragraph to introduce this section.

```html(index.html)
<!-- Testimonials
================================================== -->
<div id="testimonials">
+	<div class="container">
+		<div class="twelve columns offset-by-two">
			<h2>Who's using it?</h2>
			<p>Jott.ly has around 150,000 satisfied customers sharing and collaborating with teams throughout 35 countries. Here’s what a few had to say:</p>
+		</div>
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
+	</div>
</div>
```

We've simply add the `container` div to set our content to the center of the page, and then have added our 12-column grid to our introduction text for the section.

Now, we can add in the `one-third column` classes into a new div to segment our testimonials.

```html(index.html)
<!-- Testimonials
================================================== -->
<div id="testimonials">
	<div class="container">
		<div class="twelve columns offset-by-two">
			<h2>Who's using it?</h2>
			<p>Jott.ly has around 150,000 satisfied customers sharing and collaborating with teams throughout 35 countries. Here’s what a few had to say:</p>
		</div>
+		<div class="one-third column">
			<blockquote>
				“Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
			</blockquote>
			<div class="avatar">
				<img src="images/avatar1.jpg" />
				<p>Danny S.</p>
			</div>
+		</div>
+		<div class="one-third column">
			<blockquote>
				“Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
			</blockquote>
			<div class="avatar">
				<img src="images/avatar2.jpg" />
				<p>Jonathan M.</p>
			</div>
+		</div>
+		<div class="one-third column">
			<blockquote>
				“Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
			</blockquote>
			<div class="avatar">
				<img src="images/avatar3.jpg" />
				<p>Chloe P.</p>
			</div>
+		</div>
	</div>
</div>
```

Before each `blockquote` opening tag, you can add in a new div with the `one-third column` classes. Be sure to close that div tag too, or it won't appear correctly.

If you have the file opened in a browser, you will see the changes upon refresh. You should have three columns with the quote, avatar image and the name of the person.

### Action Section

Next, we're going to focus on getting the grid aligned for the action section. Again, follow the same steps in centering the header and paragraph introduction text. 

```html(index.html) 
<!-- Call to Action
================================================== -->
  	<div id="action">
+  	  	<div class="container">
+  	  	  	<div class="twelve columns offset-by-two">
  	  	  	  	<h2>Give it a try before you commit.</h2>
  	  	  	  	<p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
  	  	  	  	<input type="text" placeholder="Enter your email address"/>
  	  	  	  	<button type="submit">Sign Up Now</button>  
+	  	  	</div>
+  	  	</div>
  	</div>
 ```
 
Now, we need to section off our input and submit buttons to get them to fit the size we're going for. To do this, we're going to use the same concept as before, by creating a container within a container. 

```html(index.html) 
<!-- Call to Action
================================================== -->
  	<div id="action">
  	  	<div class="container">
  	  	  	<div class="twelve columns offset-by-two">
  	  	  	  	<h2>Give it a try before you commit.</h2>
  	  	  	  	<p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
+				<div class="container">
+  	  	  	  	  	<div class="row">
+  	  	  	  	  	  	<div class="eight columns alpha">
  	  	  	   	  	  	 	<input type="text" placeholder="Enter your email address"/>
+  	  	  	  	  	  	</div>
+  	  	  	  	  	  	<div class="four columns omega">
  	  	  	  	  	  	  	<button type="submit">Sign Up Now</button> 
+  	  	  	  	  	  	</div>
+  	  	  	  	  	</div>
+  	  	  	  	</div>
	  	  	</div>
  	  	</div>
  	</div>
 ```
 
Directly below your closing `p` tag, add in a `div class="container"`. Next, we're going to set up our `row` div nested inside that container.

Next, wrap your `input` field in an 8-column div with an `alpha` class so that it will remove the padding and margins from the left side. Once you close that div, you can wrap your `button` in a 4-column div with an `omega` class. This will line up your input field and submit button next to each other.

Be sure to close out all of your newly created divs or it won't appear correctly. The last part of this checkpoing, we're going to set up the footer to fit on our grid.

### Footer

We're going to section our footer into three pieces. The majority of the room will be given to our navigation links on the left side of the page. With that, we need an area for our small logo and the copyright text.

```html(index.html)   
<!-- Footer
================================================== -->
<div id="footer">
+  	<div class="container">
+  	  	<div class="twelve columns">
  	  	  	<nav>
  	  	  	  	<ul>
  	  	  	  	  	<li><a href="#">About</a></li>
  	  	  	  	  	<li><a href="#">Contact</a></li>
  	  	  	  	  	<li><a href="#">Privacy Policy</a></li>
  	  	  	  	  	<li><a href="#">Terms</a></li>
  	  	  	  	</ul>
  	  	  	</nav>
+  	  	</div>
+
+  	  	<div class="two columns">
-  	  	  	<img src="images/small_logo.png" />
+  	  	  	<img src="images/small_logo.png" alt="Jottly" />
+  	  	</div>
+
+  	  	<div class="two columns">
  	  	  	<p>&copy; 2014. Jott.ly. All Rights Reserved.</p>
+  	  	</div>
+  	</div>
</div>
```

Before anything else, wrap your content in a `container` div. Next, let's put a 12-column div around the `nav` tag inside a new div.

For the small logo and copyright text, we're going to split the remaining four columns between the two. We've section them off with `two columns` divs. 

Notice the small change for the logo image too. We've added an `alt` attribute with a value of `Jottly`. This provides some text to be displayed when the image cannot be displayed.

Now, our landing page has been fixed up to integrate the grid system from Skeleton. We should see a much cleanly aligned page as you begin scrolling down.

Next, we're going to start focusing on the styling of each section to make it look refined and finished.