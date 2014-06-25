## Header and Sections in Pricing Tiers

```html(index.html)
 	<!-- Pricing
  	================================================== -->
  	<div id="pricing">
 -		<h2>How much will it cost me?</h2>
 -		<p>It’s rather inexpensive to use Jott.ly’s suite of tools compared to several other services out there. We have several options to fit your budget and needs:</p>
 -
 -			<div class="pricebox">
 -				<h3>Individuals &amp; Family</h3>
 -				<h4>$2</h4>
 -				<p>per month/per user</p>
 -				<ul>
 -					<li>Unlimited notes</li>
 -					<li>Unlimited members</li>
 -					<li><strong>2GB</strong> of storage</li>
 -				</ul>
 -				<button>Select this plan</button>
 +		<div class="container">
 +			<div class="twelve columns offset-by-two">
 +				<h2>How much will it cost me?</h2>
 +				<p>It’s rather inexpensive to use Jott.ly’s suite of tools compared to several other services out there. We have several options to fit your budget and needs:</p>
 +			</div>
 +
 +			<div class="one-third column">
 +				<div class="pricebox">
 +					<header>
 +						<h3>Individuals &amp; Family</h3>
 +					</header>
 +					<section>
 +						<h4>$2</h4>
 +						<p>per month/per user</p>
 +						<ul>
 +							<li>Unlimited notes</li>
 +							<li>Unlimited members</li>
 +							<li><strong>2GB</strong> of storage</li>
 +						</ul>
 +						<button>Select this plan</button>
 +					</section>
 +				</div>
  			</div>
  
 -			<div class="pricebox">
 -				<h3>Small Businesses</h3>
 -				<h4>$5</h4>
 -				<p>per month/per user</p>
 -				<ul>
 -					<li>Unlimited notes</li>
 -					<li>Unlimited members</li>
 -					<li><strong>15GB</strong> of storage</li>
 -					<li>Real-time collaboration</li>
 -				</ul>
 -				<button>Select this plan</button>
 +			<div class="one-third column">
 +				<div class="pricebox">
 +					<header>
 +						<h3>Small Businesses</h3>
 +					</header>
 +					<section>
 +						<h4>$5</h4>
 +						<p>per month/per user</p>
 +						<ul>
 +							<li>Unlimited notes</li>
 +							<li>Unlimited members</li>
 +							<li><strong>15GB</strong> of storage</li>
 +							<li>Real-time collaboration</li>
 +						</ul>
 +						<button>Select this plan</button>
 +					</section>
 +				</div>
  			</div>
  
 -			<div class="pricebox">
 -				<h3>Enterprise</h3>
 -				<h4>$8</h4>
 -				<p>per month/per user</p>
 -				<ul>
 -					<li>Unlimited notes</li>
 -					<li>Unlimited members</li>
 -					<li><strong>Unlimited</strong> of storage</li>
 -					<li>Real-time collaboration</li>
 -				</ul>
 -				<button>Select this plan</button>
 +			<div class="one-third column">
 +				<div class="pricebox">
 +					<header>
 +						<h3>Enterprise</h3>
 +					</header>
 +					<section>
 +						<h4>$8</h4>
 +						<p>per month/per user</p>
 +						<ul>
 +							<li>Unlimited notes</li>
 +							<li>Unlimited members</li>
 +							<li><strong>Unlimited</strong> of storage</li>
 +							<li>Real-time collaboration</li>
 +						</ul>
 +						<button>Select this plan</button>
 +					</section>
 +				</div>
  			</div>
 +
 +		</div>
  	</div>
```