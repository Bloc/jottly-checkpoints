![](https://www.dropbox.com/s/j1ift2vmmrqr5d8/07-header-skeleton.png)

```html(index.html)
 	<!-- Header
  	================================================== -->
  	<div id="header">
 -		<img src="images/logo.png" />
 -		<nav>
 -			<ul>
 -				<li><a href="#">Sign In</a></li>
 -				<li><a href="#">Sign Up Now</a></li>
 -			</ul>
 -		</nav>
 -
 -		<h1>An easier way to write &amp; collaborate</h1>
 -		<p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
 +		<div class="container">
 +			<div class="three columns">
 +				<div class="logo">
 +					<a href="#"><img src="images/logo.png" alt="Jottly" /></a>
 +				</div>
 +			</div>
 +			<div class="thirteen columns">
 +				<nav>
 +					<ul>
 +						<li><a href="#">Sign In</a></li>
 +						<li><a href="#">Sign Up Now</a></li>
 +					</ul>
 +				</nav>
 +			</div>
 +		</div>
  
 -		<input type="text" placeholder="Enter your email address"/>
 -		<button type="submit">Sign Up Now</button>
 +		<div class="container">
 +			<div class="nine columns">
 +				<h1>An easier way to write &amp; collaborate</h1>
 +				<p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
 +
 +				<div class="container">
 +					<div class="row">
 +						<div class="five columns alpha">
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
```