## Integrating Google Fonts

![](http://cl.ly/WHVZ/11-google-fonts.png)

```html(index.html)
   ================================================== -->
  	<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1">
  
 +	<!-- Google Fonts
 +	================================================== -->
 +	<link href='http://fonts.googleapis.com/css?family=Lato:300,400,700,900,100italic,300italic,400italic,700italic,900italic' rel='stylesheet' type='text/css'>
 +
  	<!-- CSS
    ================================================== -->
  	<link rel="stylesheet" href="stylesheets/base.css">
```

```CSS(stylesheets/base.css)
 ================================================== */
  	body {
  		background: #fff;
 -		font: 14px/21px "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
 +		font: 14px/21px "Lato", "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
  		color: #444;
  		-webkit-font-smoothing: antialiased; /* Fix for webkit rendering */
  		-webkit-text-size-adjust: 100%;
 @@ -63,7 +63,7 @@
  ================================================== */
  	h1, h2, h3, h4, h5, h6 {
  		color: #181818;
 -		font-family: "Georgia", "Times New Roman", serif;
 +		font-family: "Lato", "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
  		font-weight: normal; }
```