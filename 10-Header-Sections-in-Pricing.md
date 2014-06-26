## Header and Sections in Pricing Tiers

![](http://cl.ly/WHB1/09-pricing-sections.png)

In this checkpoint, we'll apply our pricing tiers to the grid, splitting the width in three equal columns.

### Container

Like the other sections, we're going to add a `container` div to center our content on the page. We're also going to add `header` and `section` tags to each price box so we can edit the style with ease.

```html(index.html)
<!-- Pricing
================================================== -->
  	<div id="pricing">
+  	  	<div class="container">
+  	  	  	<div class="twelve columns offset-by-two">
  	  	  	  	<h2>How much will it cost me?</h2>
  	  	  	  	<p>It’s rather inexpensive to use Jott.ly’s suite of tools compared to several other services out there. We have several options to fit your budget and needs:</p>
+  	  	  	</div>
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
+  	  	</div>
  	</div>
```

We're also going to wrap our `h2` and `p` tags inside a 12-column div and offset it like before. We're doing this to keep the width smaller than the full width. With paragraphs of text, it's easier for the user to read if each line doesn't stretch across the full width of the page. Lines after lines of text can cause the eyes to tire. So tightening the width can help the readability.

### One-Third column

Next, we're going to put the price boxes across the page in three equal columns. Because we're on a 16-column grid, we can't do this with math. However, Skeleton has provided a new class of `one-third column` in order to satisfy the requirements for 3 boxes across the width of a page.


```html(index.html)
<!-- Pricing
================================================== -->
  	<div id="pricing">
  	  	<div class="container">
  	  	  	<div class="twelve columns offset-by-two">
  	  	  	  	<h2>How much will it cost me?</h2>
  	  	  	  	<p>It’s rather inexpensive to use Jott.ly’s suite of tools compared to several other services out there. We have several options to fit your budget and needs:</p>
  	  	  	</div>
+  	  	  	<div class="one-third column">
				<div class="pricebox">
				  	<h3>Individuals &amp; Family</h3>
  	  	  	  	  	<h4>$2</h4>
  	  	  	  	  	<p>per month/per user</p>
  	  	  	  	  	<ul>
  	  	  	  	  	  	<li>Unlimited notes</li>
  	  	  	  	  	  	<li>Unlimited members</li>
  	  	  	  	  	  	<li><strong>2GB</strong> of storage</li>
  	  	  	  	  	</ul>
+  	  	  	  	  	<button>Select this plan</button>
				</div>
+  			</div>
+  	  	  	<div class="one-third column">
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
+  			</div>
+			<div class="one-third column">
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
+  	  	  	</div>
		</div>
  	</div>
```

Before each `pricebox` div, we need to add a new div with classes of `one-third` and `column`, as shown above. Be sure to close those divs as well. 

> As you are writing this code, it's important for you to open the `index.html` file inside a web browser, preferably Google Chrome.

### Header and Sections

Next, we're going to set up our header for each box. This will allow us to change the styling of the name of each price plan. Below, we're going to focus on one single price box, but you will replicate these steps to each of the three boxes.

```html(index.html)
<div class="one-third column">
  	<div class="pricebox">
+  	  	<header>
  	  	  	<h3>Individuals &amp; Family</h3>
+  	  	</header>
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
```

For this, you're simply going to wrap your `h3` tags in a new tag called `header`. This is different from our `div id="header"` that we used earlier. With this HTML element, we're able to use it for multiple sections if we choose to. It simply is set to introduce a section of content. With that, we're going to section off the rest of our text elements inside the `pricebox` div. We'll do this by using the `section` HTML tag.

```html(index.html)
<div class="one-third column">
  	<div class="pricebox">
  	  	<header>
  	  	  	<h3>Individuals &amp; Family</h3>
  	  	</header>
+  	  	<section>
  	  	  	<h4>$2</h4>
  	  	  	<p>per month/per user</p>
  	  	  	<ul>
  	  	  	  	<li>Unlimited notes</li>
  	  	  	  	<li>Unlimited members</li>
  	  	  	  	<li><strong>2GB</strong> of storage</li>
  	  	  	</ul>
  	  	  	<button>Select this plan</button>
+  	  	</section>
  	  </div>
</div>
```

Before your `h4` tags and after the closing `header` tag, we will add a new element called `section`. This, like `header`, is an HTML5 specific tag. It basically allows you to section on content with ease, much like a `div`. 

Once you've done this for the first `pricebox` div, be sure to replicate to the other two, like so:

```html(index.html)
...
+  	<div class="one-third column">
  	  	<div class="pricebox">
+  	  	  	<header>
  	  	  	  	<h3>Small Businesses</h3>
+  	  	  	</header>
+  	  	  	<section>
  	  	  	  	<h4>$5</h4>
  	  	  	  	<p>per month/per user</p>
  	  	  	  	<ul>
  	  	  	  	  	<li>Unlimited notes</li>
  	  	  	  	  	<li>Unlimited members</li>
  	  	  	  	  	<li><strong>15GB</strong> of storage</li>
  	  	  	  	  	<li>Real-time collaboration</li>
  	  	  	  	</ul>
  	  	  	  	<button>Select this plan</button>
+  	  	  	</section>
  	  	</div>
+  	</div>
...
+  	<div class="one-third column">
  	  	<div class="pricebox">
+  	  	  	<header>
  	  	  	  	<h3>Enterprise</h3>
+  	  	  	</header>
+  	  	  	<section>
  	  	  	  	<h4>$8</h4>
  	  	  	  	<p>per month/per user</p>
  	  	  	  	<ul>
  	  	  	  	  	<li>Unlimited notes</li>
  	  	  	  	  	<li>Unlimited members</li>
  	  	  	  	  	<li><strong>Unlimited</strong> of storage</li>
  	  	  	  	  	<li>Real-time collaboration</li>
  	  	  	  	</ul>
  	  	  	  	<button>Select this plan</button>
+  	  	  	</section>
  	  	</div>
+  	</div>
```

Now, you should have three equal columns across the width of your page with each price box.

Next, we're going to update the testimonials section along with the action and footer.