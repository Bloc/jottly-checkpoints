## Deleting default content

![Deleting default content](http://cl.ly/WEn9/02-deleting.png)

In this checkpoint we'll replace the default content in the Skeleton template with custom HTML for Jottly's landing page.

## Removing unnecessary code

Open the Jottly folder inside a text editor like [Sublime Text 2](http://www.sublimetext.com/2). Locate `index.html` - this is the file we'll edit.

Remove the lines shown below in red, and add in the lines in green. We will add our first HTML tag — `<h1>Hello world!</h1>` — which is a header tag. You will also change the title of your page from Your Page Title Here :) to Jott.ly.

```html(index.html)
<!-- Basic Page Needs
================================================== -->
  <meta charset="utf-8">
-  <title>Your Page Title Here :)</title>
+  <title>Jott.ly</title>
  <meta name="description" content="">
  <meta name="author" content="">

  <!-- Mobile Specific Metas
  ================================================== -->
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1">

  <!-- CSS
  ================================================== -->
  <link rel="stylesheet" href="stylesheets/base.css">
  <link rel="stylesheet" href="stylesheets/skeleton.css">
  <link rel="stylesheet" href="stylesheets/layout.css">

  <!--[if lt IE 9]>
    <script src="http://html5shim.googlecode.com/svn/trunk/html5.js"></script>
  <![endif]-->

  <!-- Favicons
  ================================================== -->
  <link rel="shortcut icon" href="images/favicon.ico">
  <link rel="apple-touch-icon" href="images/apple-touch-icon.png">
  <link rel="apple-touch-icon" sizes="72x72" href="images/apple-touch-icon-72x72.png">
  <link rel="apple-touch-icon" sizes="114x114" href="images/apple-touch-icon-114x114.png">
          
 </head>
 <body>

+  <h1> Hello World! </h1>
-
-    <!-- Primary Page Layout
-    ================================================== -->
-
-    <!-- Delete everything in this .container and get started on your own site! -->
-
-      <div class="container">
-        <div class="sixteen columns">
-          <h1 class="remove-bottom" style="margin-top: 40px">Skeleton</h1>
-          <h5>Version 1.2</h5>
-          <hr />
-        </div>
-        <div class="one-third column">
-          <h3>About Skeleton?</h3>
-          <p>Skeleton is a small collection of well-organized CSS files that can help you rapidly develop sites that look beautiful at any size, be it a 17" laptop screen or an iPhone. It's based on a responsive grid, but also provides very basic CSS for typography, buttons, forms and media queries. Go ahead, resize this super basic page to see the grid in action.</p>
-        </div>
-        <div class="one-third column">
-          <h3>Three Core Principles</h3>
-          <p>Skeleton is built on three core principles:</p>
-          <ul class="square">
-            <li><strong>A Responsive Grid Down To Mobile</strong>: Elegant scaling from a browser to tablets to mobile.</li>
-            <li><strong>Fast to Start</strong>: It's a tool for rapid development with best practices</li>
-            <li><strong>Style Agnostic</strong>: It provides the most basic, beautiful styles, but is meant to be overwritten.</li>
-          </ul>
-        </div>
-        <div class="one-third column">
-          <h3>Docs &amp; Support</h3>
-          <p>The easiest way to really get started with Skeleton is to check out the full docs and info at <a href="http://www.getskeleton.com">www.getskeleton.com.</a>. Skeleton is also open-source and has a <a href="https://github.com/dhgamache/skeleton">project on git</a>, so check that out if you want to report bugs or create a pull request. If you have any questions, thoughts, concerns or feedback, please don't hesitate to email me at <a href="mailto:hi@getskeleton.com">hi@getskeleton.com</a>.</p>
-        </div>
-
-      </div><!-- container -->
-
-
-<!-- End Document
-================================================== -->
+
 </body>
 </html>
 ```

This code will display a single line of text in your browser that reads, Hello World!. Open your `index.html` inside your browser. You can do this by double-clicking the file in your file directory.

> We recommend you keep `index.html` open in your browser as you update the files. You will need to refresh your browser to view the changes.

### Pushing your changes

Again, we will push these changes to our Jottly repo. First, make sure you are still on the gh-pages branch.

```bash(Terminal)
$ git status
```

This command should display the changes and the name of the current branch. Let's add commit and push our code.

```bash(Terminal)
$ git add .
$ git commit -m "Removed default content"
$ git push origin gh-pages
```

Next, we'll add custom headers and images to `index.html`.
