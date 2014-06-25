## Deleting default content

![Deleting default content](http://cl.ly/WEn9/02-deleting.png)

In this checkpoint, we will remove the default content inside the Skeleton template so we can begin adding our HTML to the landing page for Jott.ly.

## Removing unnecessary code

Open up your `Jottly` folder inside a text editor like [Sublime Text 2](http://www.sublimetext.com/2). Then locate the `index.html` file, which we'll be editing.

Next, remove the lines shown below in red, and add in the ones in green. We will be adding our first HTML tag — `<h1>Hello world!</h1>` — which is a header tag. You will also change the title of your page from `Your Page Title Here :)` to `Jott.ly`.

```html(index.html)
<!-- Basic Page Needs
   ================================================== -->
        <meta charset="utf-8">
-       <title>Your Page Title Here :)</title>
+       <title>Jott.ly</title>
        <meta name="description" content="">
        <meta name="author" content="">
 </head>
 <body>
 
+  <h1> Hello World </h1>
-
-       <!-- Primary Page Layout
-       ================================================== -->
-
-       <!-- Delete everything in this .container and get started on your own site! -->
-
-       <div class="container">
-               <div class="sixteen columns">
-                       <h1 class="remove-bottom" style="margin-top: 40px">Skeleton</h1>
-                       <h5>Version 1.2</h5>
-                       <hr />
-               </div>
-               <div class="one-third column">
-                       <h3>About Skeleton?</h3>
-                       <p>Skeleton is a small collection of well-organized CSS files that can help you rapidly
-               </div>
-               <div class="one-third column">
-                       <h3>Three Core Principles</h3>
-                       <p>Skeleton is built on three core principles:</p>
-                       <ul class="square">
-                               <li><strong>A Responsive Grid Down To Mobile</strong>: Elegant scaling from a b
-                               <li><strong>Fast to Start</strong>: It's a tool for rapid development with best
-                               <li><strong>Style Agnostic</strong>: It provides the most basic, beautiful styl
-                       </ul>
-               </div>
-               <div class="one-third column">
-                       <h3>Docs &amp; Support</h3>
-                       <p>The easiest way to really get started with Skeleton is to check out the full docs an
-               </div>
-
-       </div><!-- container -->
-
-
-<!-- End Document
-================================================== -->
+
 </body>
 </html>
 ```
 
Once you have completed this, you should see a single line of text in your browser that says, 'Hello world!'. 

### Pushing your changes

Again, we will push your changes to your Github repo so that we store the latest code.

```bash(Terminal)
$ git add .
$ git commit -m "Removed default content"
$ git push
```