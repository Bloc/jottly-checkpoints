## Deleting default content

<center>![Deleting default content](https://bloc-global-assets.s3.amazonaws.com/images-design/blocbooks/jottly/HelloWorld.png)</center>

In this checkpoint we'll replace the default content in the Skeleton template with custom HTML for Jottly's landing page.

### Cleanup

Open the Jottly folder inside a text editor like [Sublime Text 2](http://www.sublimetext.com/2). Locate `index.html` - this is the file we'll edit.

Remove the lines shown below in red, and add in the lines in green. We will add our first HTML tag — `<h1>Hello world!</h1>` — which is a header tag. You will also change the title of the page from "Your page title here :)" to "Jott.ly".

```html(index.html)
<!DOCTYPE html>
<html lang="en">
<head>

  <!-- Basic Page Needs
  –––––––––––––––––––––––––––––––––––––––––––––––––– -->
  <meta charset="utf-8">
+  <title>Jott.ly</title>
-  <title>Your page title here :)</title>
  <meta name="description" content="">
  <meta name="author" content="">

  <!-- Mobile Specific Metas
  –––––––––––––––––––––––––––––––––––––––––––––––––– -->
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1">

  <!-- FONT
  –––––––––––––––––––––––––––––––––––––––––––––––––– -->
  <link href='http://fonts.googleapis.com/css?family=Raleway:400,300,600' rel='stylesheet' type='text/css'>

  <!-- CSS
  –––––––––––––––––––––––––––––––––––––––––––––––––– -->
  <link rel="stylesheet" href="css/normalize.css">
  <link rel="stylesheet" href="css/skeleton.css">

  <!-- Favicon
  –––––––––––––––––––––––––––––––––––––––––––––––––– -->
  <link rel="icon" type="image/png" href="images/favicon.png" />

</head>
<body>
+ <h1>Hello World!</h1>
-  <!-- Primary Page Layout
-  –––––––––––––––––––––––––––––––––––––––––––––––––– -->
-  <div class="container">
-    <div class="row">
-      <div class="one-half column" style="margin-top: 25%">
-        <h4>Basic Page</h4>
-        <p>This index.html page is a placeholder with the CSS, font and favicon. It's just waiting for you to add some content! If you need some help hit up the <a href="http://www.getskeleton.com">Skeleton documentation</a>.</p>
-      </div>
-    </div>
-  </div>

<!-- End Document
  –––––––––––––––––––––––––––––––––––––––––––––––––– -->
</body>
</html>
```

Next, we'll add custom headers and images to `index.html`.
