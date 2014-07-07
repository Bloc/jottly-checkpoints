## Integrating Google Fonts

![](http://cl.ly/WHVZ/11-google-fonts.png)

In this checkpoint we'll implement [Google Fonts](http://www.google.com/fonts), which contains hundreds of open-sourced fonts. We'll use [Lato](https://www.google.com/fonts/specimen/Lato) as our primary typeface for Jottly. Upon selecting a typeface, we'll specify the font weight and type as well.

Let's add the link to Google Fonts and specify the font we'd like to use:

```html(index.html)
...
 <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1">
+
+<!-- Google Fonts
+================================================== -->
+<link href='http://fonts.googleapis.com/css?family=Lato:300,400,700,900,100italic,300italic,400italic,700italic,900italic' rel='stylesheet' type='text/css'>
+
 <!-- CSS
 ================================================== -->
 <link rel="stylesheet" href="stylesheets/base.css">
```

Make sure this code is placed in the <head> section of the landing page, and before the CSS section. It will need to be loaded before the CSS so we can reference it in our stylesheets.

Open up the base.css file inside your text editor. There are two lines we are going to change to include Lato as our main typeface within the site:

```css(stylesheets/base.css)
 ================================================== */
body {
  background: #fff;
- font: 14px/21px "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
+ font: 14px/21px "Lato", "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
  color: #444;
  -webkit-font-smoothing: antialiased; /* Fix for webkit rendering */
  -webkit-text-size-adjust: 100%;
...
  ================================================== */
h1, h2, h3, h4, h5, h6 {
  color: #181818;
- font-family: "Georgia", "Times New Roman", serif;
+ font-family: "Lato", "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-weight: normal; }
```

Under the body tag, we add "Lato", before Helvetica Neue. The order of typefaces provides the user with backups in case the proper font doesn't load.

In this case, Lato is our primary choice, with Helvetica Neue, Helvetica and Arial as back-up options. And if none of those are able to render, we'll use the browser default of sans-serif.

The second line we changed addresses the styling of the headers. Instead of the default serif typefaces, we'll use the same hierarchy of font options from the body font above.

Our landing page should now have a nice-looking sans serif typeface.

### Github

Push your changes to Github:

```bash(Terminal)
$ git add .
$ git commit -m "Using Google Fonts"
$ git push origin gh-pages
```

Next, we'll begin to style each section of our page.
