## Integrating Google Fonts

<center>![Google Fonts Lato](https://bloc-global-assets.s3.amazonaws.com/images-design/blocbooks/jottly/jottlygooglefonts.png)</center>

In this checkpoint we'll implement a different [Google Font](http://www.google.com/fonts), which contains hundreds of open-sourced fonts. We'll use [Lato](https://www.google.com/fonts/specimen/Lato) as our primary typeface for Jottly instead of Skeleton's default - Raleway. Upon selecting a typeface, we'll specify the font weight and type as well.

Let's change the Google Fonts link to specify the new font we'd like to use:

```html(index.html)
...
<meta name="viewport" content="width=device-width, initial-scale=1">

<!-- FONT
–––––––––––––––––––––––––––––––––––––––––––––––––– -->
- <link href="//fonts.googleapis.com/css?family=Raleway:400,300,600" rel="stylesheet" type="text/css">
+ <link href='http://fonts.googleapis.com/css?family=Lato:300,400,700,900,100italic,300italic,400italic,700italic,900italic' rel='stylesheet' type='text/css'>
```

Make sure this code is placed in the <head> section of the landing page, and before the CSS section. It will need to be loaded before the CSS so we can reference it in our stylesheets.

Open up the base.css file inside your text editor. There are two lines we are going to change to include Lato as our main typeface within the site:

```css(css/skeleton.css)
body {
  font-size: 1.5em; /* currently ems cause chrome bug misinterpreting rems on body element */
  line-height: 1.6;
  font-weight: 400;
-  font-family: "Raleway", "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
+  font-family: "Lato", "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
  color: #222; }
```

Under the body tag, we replace "Raleway" with "Lato", before Helvetica Neue. The order of typefaces provides the user with backups in case the proper font doesn't load.

In this case, Lato is our primary choice, with Helvetica Neue, Helvetica and Arial as back-up options. And if none of those are able to render, we'll use the browser default of sans-serif.

Our landing page should now have a nice-looking sans serif typeface.

Next, we'll begin to style each section of our page.
