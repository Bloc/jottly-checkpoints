## Adding the grid to the Benefits section

![](http://cl.ly/WHCg/08-benefits-skeleton.png)

In this checkpoint we'll apply a grid layout to the Benefits section. In the process we'll use a new class that offsets columns. Let's start by creating a new container and nesting the offset div:

```html(index.html)
  <!-- Benefits
  ================================================== -->
  <div id="benefits">
+   <div class="container">
+     <div class="twelve columns offset-by-two">
  	    <h2>What is Jott.ly exactly?</h2>
  	  	<p>Our web application allows you to create documents with real-time editing and collaborating capabilities, while storing content and information to share with others.</p>
+     </div>
		  <img src="images/app.png" alt="Jottly's Web Application" />
+	 </div>
  </div>
```

The offset on the 12 column div centers its contained content by two columns on either side.

```html(index.html)
  <!-- Benefits
  ================================================== -->
  <div id="benefits">
    <div class="container">
  	  <div class="twelve columns offset-by-two">
  	    <h2>What is Jott.ly exactly?</h2>
  	  	<p>Our web application allows you to create documents with real-time editing and collaborating capabilities, while storing content and information to share with others.</p>
  	  </div>
-     <img src="images/app.png" alt="Jottly's Web Application" />
+     <div class="fourteen columns offset-by-one">
+	     <img class="scale-with-grid" src="images/app.png" alt="Jottly's Web Application" />
+	   </div>
	  </div>
  </div>
```

We've wrapped the img tag inside a 14 column div. We've once again used an offset to center the contained content.

We added the scale-with-grid class to our img tag. This class allows images to fit to the grid on mobile devices, laptops and large-screen monitors.

### Pushing your changes

Push your changes to Github:

```bash(Terminal)
$ git add .
$ git commit -m "Integrated a grid layout for the benefits section"
$ git push origin gh-pages
```

Next we'll work on improving the pricing tier layouts.
