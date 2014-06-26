## Styling the header

![](http://cl.ly/WHHY/12-style-header.png)

```html(index.html)
 				<nav>
  					<ul>
  						<li><a href="#">Sign In</a></li>
 -						<li><a href="#">Sign Up Now</a></li>
 +						<li><a class="btn" href="#">Sign Up Now</a></li>
  					</ul>
  				</nav>
  			</div>
  		</div>
  
  		<div class="container">
 -			<div class="nine columns">
 +			<div class="nine columns headertext">
  				<h1>An easier way to write &amp; collaborate</h1>
  				<p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
  
```

```css(stylesheets/base.css)
+#header nav {
 +	text-align: right;
 +	margin-top: 2em;
 +}
 +#header nav ul li {
 +	display:inline-block;
 +}
 +#header nav ul li a {
 +	color:#fff;
 +	text-transform: uppercase;
 +	text-decoration: none;
 +	padding:0.75em 2em;
 +}
 +#header nav ul li a.btn {
 +	-moz-border-radius: 8px;
 +	-webkit-border-radius: 8px;
 +	border-radius: 8px; /* border radius */
 +	border:2px solid #fff;
 +}
 +#header nav ul li a.btn:hover {
 +	background:#fff;
 +	color:#009be8;
 +}
 +#header .headertext {
 +	margin-top: 10em;
 +}
 +#header h1 {
 +	color:#fff;
 +	font-weight:300;
 +	font-size:4.5em;
 +	line-height: 1;
 +	text-shadow: 0 1px 2px rgba(0,0,0,.2);
 +	margin-bottom: 0.3em;
 +}
 +#header p {
 +	color:#d5d5d5;
 +	font-size:1.33em;
 +	line-height: 1.5;
 +	text-shadow: 0 1px 2px rgba(0,0,0,.2);
 +	margin-bottom: 1.2em;
 +}
 +#header p strong {
 +	color:#fff;
 +}
```