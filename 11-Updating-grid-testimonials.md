## Updating grids for Testimonials, Action and Footer

![](http://cl.ly/WHRe/10-testimonials.png)

```html(index.html)
<!-- Testimonials
================================================== -->
<div id="testimonials">
+	<div class="container">
+		<div class="twelve columns offset-by-two">
			<h2>Who's using it?</h2>
			<p>Jott.ly has around 150,000 satisfied customers sharing and collaborating with teams throughout 35 countries. Here’s what a few had to say:</p>
 +		</div>
 +		<div class="one-third column">
 -		<blockquote>
 -			“Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
 -		</blockquote>
 -		<div class="avatar">
 -			<img src="images/avatar1.jpg" />
 -			<p>Danny S.</p>
 -		</div>
 
  
 -		<blockquote>
 -			“Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
 -		</blockquote>
 -		<div class="avatar">
 -			<img src="images/avatar2.jpg" />
 -			<p>Jonathan M.</p>
 -		</div>
 +			<div class="one-third column">
 +				<blockquote>
 +					“Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
 +				</blockquote>
 +				<div class="avatar">
 +					<img src="images/avatar1.jpg" />
 +					<p>Danny S.</p>
 +				</div>
 +			</div>
  
 -		<blockquote>
 -			“Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
 -		</blockquote>
 -		<div class="avatar">
 -			<img src="images/avatar3.jpg" />
 -			<p>Chloe P.</p>
 -		</div>
 +			<div class="one-third column">
 +				<blockquote>
 +					“Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
 +				</blockquote>
 +				<div class="avatar">
 +					<img src="images/avatar2.jpg" />
 +					<p>Jonathan M.</p>
 +				</div>
 +			</div>
  
 +			<div class="one-third column">
 +				<blockquote>
 +					“Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.
 +				</blockquote>
 +				<div class="avatar">
 +					<img src="images/avatar3.jpg" />
 +					<p>Chloe P.</p>
 +				</div>
 +			</div>
 +		</div>
  	</div>
  
  	<!-- Call to Action
  	================================================== -->
  	<div id="action">
 -		<h2>Give it a try before you commit.</h2>
 -		<p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
 -		
 -		<input type="text" placeholder="Enter your email address"/>
 -		<button type="submit">Sign Up Now</button>				
 +		<div class="container">
 +			<div class="twelve columns offset-by-two">
 +				<h2>Give it a try before you commit.</h2>
 +				<p>You can test drive Jott.ly before deciding on one of our plans. Just give us your email address, and we'll send you the details:</p>
 +				<div class="container">
 +					<div class="row">
 +						<div class="eight columns alpha">
 +							<input type="text" placeholder="Enter your email address"/>
 +						</div>
 +						<div class="four columns omega">
 +							<button type="submit">Sign Up Now</button>	
 +						</div>
 +					</div>
 +				</div>
 +			</div>
 +		</div>
  	</div>
  
  	<!-- Footer
  	================================================== -->
  	<div id="footer">
 -		<nav>
 -			<ul>
 -				<li><a href="#">About</a></li>
 -				<li><a href="#">Contact</a></li>
 -				<li><a href="#">Privacy Policy</a></li>
 -				<li><a href="#">Terms</a></li>
 -			</ul>
 -		</nav>
 -		<img src="images/small_logo.png" />
 -		<p>&copy; 2014. Jott.ly. All Rights Reserved.</p>
 +		<div class="container">
 +			<div class="twelve columns">
 +				<nav>
 +					<ul>
 +						<li><a href="#">About</a></li>
 +						<li><a href="#">Contact</a></li>
 +						<li><a href="#">Privacy Policy</a></li>
 +						<li><a href="#">Terms</a></li>
 +					</ul>
 +				</nav>
 +			</div>
 +
 +			<div class="two columns">
 +				<img src="images/small_logo.png" alt="Jottly" />
 +			</div>
 +
 +			<div class="two columns">
 +				<p>&copy; 2014. Jott.ly. All Rights Reserved.</p>
 +			</div>
 +		</div>
  	</div>
```