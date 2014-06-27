## Integrating Google Fonts

![](http://cl.ly/WHVZ/11-google-fonts.png)

In this checkpoint, we're going to implement [Google Fonts](http://www.google.com/fonts), which contains hundreds of open-sourced fonts you can use within your web sites with ease.

### Making your selection

We've landed on using [Lato](https://www.google.com/fonts/specimen/Lato) as our primary typeface in this design. Upon selecting a typeface you like, you can choose one or many font weights and types. Google Fonts makes it easy to grab the ones you want, and add them quickly to your site. You start by adding them to a 'Collection'. Once that is complete, you can select to 'Use' the typeface, which will then provide you with the code to implement.

```html(index.html)
...
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1">
+
+	<!-- Google Fonts
+	================================================== -->
+	<link href='http://fonts.googleapis.com/css?family=Lato:300,400,700,900,100italic,300italic,400italic,700italic,900italic' rel='stylesheet' type='text/css'>
+
  	<!-- CSS
    ================================================== -->
  	<link rel="stylesheet" href="stylesheets/base.css">
```

We've copied and pasted in the code (as you can grab from above). This is basically a link to a stylesheet available from Google. We want to make sure to place this in the `<head>` of your `index.html` file, and **before** your CSS section. It will need to be loaded before the CSS so we can call it out in the styles files.

Next, we need to update our CSS in order for Lato to show up on your site.

### Updating in CSS

Open up the `base.css` file inside a text editor, like Sublime Text 2. There are two lines we are going to change to include Lato as our main typeface within the site.

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

Under the `body` tag, we add in `"Lato",` before Helvetica Neue. The order of typefaces provides the user with backups in case the proper font cannot load. So for this case, Lato is our primary choice, with Helvetica Neue, Helvetica and Arial as a fail-safe. And if none of those are able to render, we add in `sans-serif` to let the browser know to give us the default sans serif typeface available.

However, by adding our link inside the HTML and updating the CSS, we should have no issues with our fonts loading.

The second line we change is targeting the styling of the headers — `h1, h1, h3, h4, h5, h6`. Instead of the default serif typefaces, we're going to copy and paste our choices from earlier to here, in the same order.

Now, we should see our site updated to have a nice, elegant sans serif typeface. If you're viewing your site in Chrome, you can right click on any of the text elements, and using Inspect Element, discover if the right typeface is being loaded.

Next, we're going to move onto styling our page, section-by-section.