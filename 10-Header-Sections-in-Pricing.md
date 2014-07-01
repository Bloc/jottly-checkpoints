## Improving the pricing tier layout

![](http://cl.ly/WHB1/09-pricing-sections.png)

In this checkpoint we'll apply a grid layout to the pricing section.

### Container

Like the other sections, we'll add a container div to center our content on the page. We'll also add header and section tags to each price div so we can edit the style with ease.

```html(index.html)
  <!-- Pricing
  ================================================== -->
  <div id="pricing">
+   <div class="container">
+     <div class="twelve columns offset-by-two">
  	    <h2>How much will it cost me?</h2>
  	  	<p>It’s rather inexpensive to use Jott.ly’s suite of tools compared to several other services out there. We have several options to fit your budget and needs:</p>
+     </div>
  	  <div class="pricebox">
  	    <h3>Individuals &amp; Family</h3>
  	    <h4>$2</h4>
  	  	<p>per month/per user</p>
  	  	<ul>
  	  	  <li>Unlimited notes</li>
  	  	  <li>Unlimited members</li>
  	  	  <li><strong>2GB</strong> of storage</li>
  	  	</ul>
  	    <button>Select this plan</button>
  	  </div>
  	  <div class="pricebox">
  	    <h3>Small Businesses</h3>
    	  <h4>$5</h4>
  	  	<p>per month/per user</p>
  	  	<ul>
  	  	  <li>Unlimited notes</li>
  	  	  <li>Unlimited members</li>
  	  	  <li><strong>15GB</strong> of storage</li>
  	  	  <li>Real-time collaboration</li>
  	  	</ul>
  	  	<button>Select this plan</button>
  	  </div>
  	  <div class="pricebox">
  	  	<h3>Enterprise</h3>
  	  	<h4>$8</h4>
  	  	<p>per month/per user</p>
  	  	<ul>
  	  	  <li>Unlimited notes</li>
  	  	  <li>Unlimited members</li>
  	  	  <li><strong>Unlimited</strong> of storage</li>
  	  	  <li>Real-time collaboration</li>
  	  	</ul>
  	  	<button>Select this plan</button>
  	  </div>
+   </div>
  </div>
```

We wrapped the h2 and p tags inside a 12 column div and offset it. The offset will keep the width smaller than the container width. With paragraphs of text, it's easier for the user to read if each line doesn't stretch across the full width of the page.

### One-Third column

Next, we'll place the price boxes across the page in three equal columns. Because we're using a 16-column grid, we can't do this using whole number column specifications. However, Skeleton provides a class named "one-third column" which will divide the page up evenly.

```html(index.html)
  <!-- Pricing
  ================================================== -->
  <div id="pricing">
    <div class="container">
      <div class="twelve columns offset-by-two">
  	    <h2>How much will it cost me?</h2>
  	    <p>It’s rather inexpensive to use Jott.ly’s suite of tools compared to several other services out there. We have several options to fit your budget and needs:</p>
  	  </div>
+  	 <div class="one-third column">
				<div class="pricebox">
				  <h3>Individuals &amp; Family</h3>
  	  	  <h4>$2</h4>
  	  	  <p>per month/per user</p>
  	  	  <ul>
  	  	    <li>Unlimited notes</li>
  	  	  	<li>Unlimited members</li>
  	  	  	<li><strong>2GB</strong> of storage</li>
  	  	  </ul>
   	  	 <button>Select this plan</button>
				</div>
+  	 </div>
+  	 <div class="one-third column">
  	    <div class="pricebox">
  	  	  <h3>Small Businesses</h3>
  	  	  <h4>$5</h4>
  	  	  <p>per month/per user</p>
  	  	  <ul>
  	  	    <li>Unlimited notes</li>
  	  	  	<li>Unlimited members</li>
  	  	  	<li><strong>15GB</strong> of storage</li>
  	  	  	<li>Real-time collaboration</li>
  	  	  </ul>
  	  	  <button>Select this plan</button>
  	  	</div>
+  	 </div>
+		 <div class="one-third column">
			  <div class="pricebox">
  	  	  <h3>Enterprise</h3>
  	  	  <h4>$8</h4>
  	  	  <p>per month/per user</p>
  	  	  <ul>
  	  	    <li>Unlimited notes</li>
  	  	  	<li>Unlimited members</li>
  	  	  	<li><strong>Unlimited</strong> of storage</li>
  	  	  	<li>Real-time collaboration</li>
  	  	  </ul>
  	  	  <button>Select this plan</button>
  	  	</div>
+  	 </div>
		</div>
  </div>
```

> As you are writing this code, it's important for you to open the index.html file inside a web browser, preferably Google Chrome. You can check the results of your changes locally before pushing to Github.

### Header and Sections

Next, we'll create header for each box. The headers will allow us to change the styling of the name of each price plan.

```html(index.html)
       <div class="one-third column">
         <div class="pricebox">
+          <header>
  	         <h3>Individuals &amp; Family</h3>
+  	      </header>
  	       <h4>$2</h4>
  	       <p>per month/per user</p>
  	       <ul>
  	          <li>Unlimited notes</li>
  	  	      <li>Unlimited members</li>
  	  	      <li><strong>2GB</strong> of storage</li>
  	        </ul>
  	      <button>Select this plan</button>
  	    </div>
      </div>
			<div class="one-third column">
				<div class="pricebox">
+				 <header>
						<h3>Small Businesses</h3>
+				 </header>
					<h4>$5</h4>
					<p>per month/per user</p>
					<ul>
						<li>Unlimited notes</li>
						<li>Unlimited members</li>
						<li><strong>15GB</strong> of storage</li>
						<li>Real-time collaboration</li>
					</ul>
					<button>Select this plan</button>
				</div>
			</div>
			<div class="one-third column">
				<div class="pricebox">
+				 <header>
						<h3>Enterprise</h3>
+				 </header>
					<h4>$8</h4>
					<p>per month/per user</p>
					<ul>
						<li>Unlimited notes</li>
						<li>Unlimited members</li>
						<li><strong>Unlimited</strong> storage</li>
		        <li>Real-time collaboration</li>
					</ul>
					<button>Select this plan</button>
				</div>
			</div>  
```

We wrapped the h3 tags in a new HTML element named header. This is different from the div id="header" that we used earlier. With the header element, we're able to reuse the same style for multiple sections.

Let's section off the rest of the text elements inside the pricebox div. This will allow us to style the pricing plans using the same element. Notice the use of the HTML section element.

```html(index.html)
			<div class="one-third column">
				<div class="pricebox">
					<header>
						<h3>Individuals &amp; Family</h3>
					</header>
+				 <section>
			      <h4>$2</h4>
			      <p>per month/per user</p>
						<ul>
			      	<li>Unlimited notes</li>
			        <li>Unlimited members</li>
			        <li><strong>2GB</strong> of storage</li>
			      </ul>
			      <button>Select this plan</button>
+				 </section>
		    </div>
			</div>
			<div class="one-third column">
				<div class="pricebox">
					<header>
						<h3>Small Businesses</h3>
					</header>
+				 <section>
						<h4>$5</h4>
						<p>per month/per user</p>
						<ul>
							<li>Unlimited notes</li>
							<li>Unlimited members</li>
							<li><strong>15GB</strong> of storage</li>
							<li>Real-time collaboration</li>
						</ul>
						<button>Select this plan</button>
+				 </section>
				</div>
			</div>
			<div class="one-third column">
				<div class="pricebox">
					<header>
						<h3>Enterprise</h3>
					</header>
+				 <section>
						<h4>$8</h4>
						<p>per month/per user</p>
						<ul>
							<li>Unlimited notes</li>
							<li>Unlimited members</li>
							<li><strong>Unlimited</strong> storage</li>
			        <li>Real-time collaboration</li>
						</ul>
						<button>Select this plan</button>
+				 </section>
				</div>
			</div>
```

There should be three equal columns across the width of the page - one for each price box.

### Pushing your changes

Push your changes to Github:

```bash(Terminal)
$ git add .
$ git commit -m "Improved pricing tier layout"
$ git push origin gh-pages
```

Next we'll update the testimonials section, the call-to-action and footer.
