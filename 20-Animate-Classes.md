## Updating HTML to include Animate classes

![Animation](http://cl.ly/WGmd/jottly-animate1.gif)

```html(index.html)
<!-- Header
  	================================================== -->
 -	<div id="header">
 +	<div id="header" class="animated fadeInDown">
  		<div class="container">
  			<div class="three columns">
  				<div class="logo">
 @@ -59,7 +60,7 @@
  		</div>
  
  		<div class="container">
 -			<div class="nine columns headertext">
 +			<div class="nine columns headertext animated fadeInDown">
  				<h1>An easier way to write &amp; collaborate</h1>
  				<p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
  

```