## Adding the grid to the Benefits section

![](http://cl.ly/WHCg/08-benefits-skeleton.png)

In this checkpoint, we're going to structure the Benefits section to fit on the grid from Skeleton. We're going to use another new `class` that offsets columns.

```html(index.html)
 	<!-- Benefits
  	================================================== -->
  	<div id="benefits">
 -		<h2>What is Jott.ly exactly?</h2>
 -		<p>Our web application allows you to create documents with real-time editing and collaborating capabilities, while storing content and information to share with others.</p>
 -		
 -		<img src="images/app.png" alt="Jottly's Web Application" />
 +		<div class="container">
 +			<div class="twelve columns offset-by-two">
 +				<h2>What is Jott.ly exactly?</h2>
 +				<p>Our web application allows you to create documents with real-time editing and collaborating capabilities, while storing content and information to share with others.</p>
 +			</div>
 +			<div class="fourteen columns offset-by-one">
 +				<img class="scale-with-grid" src="images/app.png" alt="Jottly's Web Application" />
 +			</div>
 +		</div>
  	</div>
```