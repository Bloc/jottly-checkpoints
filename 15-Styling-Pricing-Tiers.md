## Styling the Pricing Tiers

```html(index.html)
 						<h3>Individuals &amp; Family</h3>
  					</header>
  					<section>
 -						<h4>$2</h4>
 -						<p>per month/per user</p>
 +						<h4><span>$</span>2</h4>
 +						<p>per month<br/>/per user</p>
  						<ul>
  							<li>Unlimited notes</li>
  							<li>Unlimited members</li>
 @@ -119,13 +119,13 @@
  			</div>
  
  			<div class="one-third column">
 -				<div class="pricebox">
 +				<div class="pricebox deal">
  					<header>
  						<h3>Small Businesses</h3>
  					</header>
  					<section>
 -						<h4>$5</h4>
 -						<p>per month/per user</p>
 +						<h4><span>$</span>5</h4>
 +						<p>per month<br/>/per user</p>
  						<ul>
  							<li>Unlimited notes</li>
  							<li>Unlimited members</li>
 @@ -143,8 +143,8 @@
  						<h3>Enterprise</h3>
  					</header>
  					<section>
 -						<h4>$8</h4>
 -						<p>per month/per user</p>
 +						<h4><span>$</span>8</h4>
 +						<p>per month<br/>/per user</p>
  						<ul>
  							<li>Unlimited notes</li>
  							<li>Unlimited members</li>
```

```css(stylesheets/base.css)
 	padding:4em 0 0;
  	text-align: center;
  }
 -#benefits h2, #testimonials h2 {
 +#benefits h2 {
  	color:#009be8;
  	font-weight: 300;
  }
 -#benefits p, #testimonials p {
 +#benefits p {
  	color:#9d9d9d;
  	font-size:1.2em;
 +}
 +
 +/* Pricing */
 +#pricing {
 +	background:#009be8;
 +	padding:4em 0;
 +	text-align: center;
 +}
 +#pricing h2 {
 +	color:#fff;
 +	font-weight:300;
 +	text-shadow: 0 1px 2px rgba(0,0,0,.2);
 +}
 +#pricing p {
 +	color:#fff;
 +	text-shadow: 0 1px 2px rgba(0,0,0,.2);
 +	font-size:1.2em;
 +}
 +.pricebox {
 +	background-color: #fff;
 +	-moz-box-shadow: 0 1px 3px rgba(0,0,0,.2);
 +	-webkit-box-shadow: 0 1px 3px rgba(0,0,0,.2);
 +	box-shadow: 0 1px 3px rgba(0,0,0,.2);
 +	margin-top:3em;
 +	height:400px;
 +	position: relative;
 +}
 +.pricebox.deal {
 +	margin-top:2em;
 +	height:430px;
 +}
 +.pricebox header {
 +	background-color: #f1f1f1;
 +	-moz-box-shadow: 0 1px 3px rgba(0,0,0,.2);
 +	-webkit-box-shadow: 0 1px 3px rgba(0,0,0,.2);
 +	box-shadow: 0 1px 3px rgba(0,0,0,.2);
 +	padding:1em 0;
 +	margin-bottom:2em;
 +}
 +.pricebox header h3 {
 +	color:#4d4d4d;
 +	font-size:1.4em;
 +	text-transform: uppercase;
 +	margin:0;
 +	font-weight: 600;
 +}
 +.pricebox section button {
 +	background:#2ecc71;
 +	position:absolute;
 +	bottom:1em;
 +	width:90%;
 +	left:0;
 +	right:0;
 +	margin:0 auto;
 +	text-align: center;
 +}
 +.pricebox section button:hover {
 +	background:#1fae5c;
 +}
 +.pricebox section h4 {
 +	display:inline-block;
 +	color:#009be8;
 +	font-size: 6em;
 +	font-weight: 900;
 +	vertical-align: bottom;
 +}
 +.pricebox section h4 span {
 +	font-size:0.5em;
 +	line-height: 1;
 +	vertical-align: top;
 +}
 +#pricing .pricebox section p {
 +	display:inline-block;
 +	color:#9d9d9d;
 +	text-shadow:none;
 +	line-height: 1;
 +	position:relative;
 +	top:1em;
 +	font-size:1.1em;
 +}
 +.pricebox section ul {
 +	margin-top:3em;
 +}
 +.pricebox section ul li {
 +	font-size:1.2em;
 +	margin-bottom: 1.2em;
  }
```