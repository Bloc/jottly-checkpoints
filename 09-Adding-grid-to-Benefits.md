## Adding the grid to the Benefits section

![](http://cl.ly/WHCg/08-benefits-skeleton.png)

In this checkpoint, we're going to structure the Benefits section to fit on the grid from Skeleton. We're going to use another new `class` that offsets columns.

```html(index.html)
 	<!-- Benefits
  	================================================== -->
  	<div id="benefits">
+  	  	<div class="container">
+  	  	  	<div class="twelve columns offset-by-two">
  	  	  	  	<h2>What is Jott.ly exactly?</h2>
  	  	  	  	<p>Our web application allows you to create documents with real-time editing and collaborating capabilities, while storing content and information to share with others.</p>
+  	  	  	</div>
		    <img src="images/app.png" alt="Jottly's Web Application" />
+		</div>
  	</div>
```

First, we're going to nest a `container` div inside of our `benefits` div. Before the `h2`, you will add a 12-column div. Here, we're adding an offset of 2 columns. This will offset your div 2 columns on the right and 2 columns on the left. This allows you to center your content. In this case, 12+2+2 = 16. We close our div and are ready to move onto setting up the size of the image.

```html(index.html)
 	<!-- Benefits
  	================================================== -->
  	<div id="benefits">
  	  	<div class="container">
  	  	  	<div class="twelve columns offset-by-two">
  	  	  	  	<h2>What is Jott.ly exactly?</h2>
  	  	  	  	<p>Our web application allows you to create documents with real-time editing and collaborating capabilities, while storing content and information to share with others.</p>
  	  	  	</div>
+			<div class="fourteen columns offset-by-one">
+				<img class="scale-with-grid" src="images/app.png" alt="Jottly's Web Application" />
+			</div>
		</div>
  	</div>
```

We've taken our `img` tag, and wrapped it inside a 14 column div. Here again, we're using offset to give the proper spacing on the right and left sides (14+1+1 = 16).

We've added on other value to the class of the `img` tag. The class `scale-with-grid` is a value created for Skeleton that allows images to fit to the grid, no matter where the site is viewed or how wide the browser window is. This will images to scale with the site on any device — mobile to large desktop.

Next, let's work on fixing up the pricing tiers.