## Integrating the Skeleton Grid with the header

![](http://cl.ly/WGOc/07-header-skeleton.png)

In this checkpoint, we're going to begin integrating Skeleton's grid to give our landing page some structure. We'll do this by reading through the documentation and using the `stylesheets/skeleton.css` file.

### Container class

One of the most important snippets you'll utilize when building out this site is a `div` with the class of 'container'. This defines the width of the content. If you look at the `skeleton.css` file in `stylesheets`, you will see the `.container` class defined. We'll get more into the CSS later on, but you can see the width is defined as 960 pixels. Skeleton is based on the 960 grid system. It's based on a 16-column grid, meaning 16 total columns will fill the width of the page. This is important to remember as you begin building out the components of the page. 

Columns will be used within, or nested, inside the `.container` div.

Let's get started. First we're going to concentrate on the top of the page, which consists of the logo and the navigation.

```html(index.html)
<!-- Header
================================================== -->
<div id="header">
-     <img src="images/logo.png" />
+     <div class="container">
+          <div class="three columns">
+               <div class="logo">
+                    <a href="#"><img src="images/logo.png" alt="Jottly" /></a>
+               </div>
+          </div>
...
+     </div>
...
```

First, we begin by adding a `div` with a `class` of 'container'. Next, we wrap the logo in two divs nested. We do this so we can edit with CSS when necessary. The first `div` is for our columns, which we've defined as `three columns`. Within the class, if you have more than one class, you add a space between the two varying classes. By looking at `skeleton.css`, you can see in order for the columns to render, you must include both the number, and the class of 'columns'. Next, we add a new `div` with a `class` of 'logo'. And then we wrap the image tag in an anchor tag, so it becomes a link back to the home page in all instances.

Next, we're going to focus on our navigation.

```html(index.html)
<!-- Header
================================================== -->
<div id="header">
     <div class="container">
          <div class="three columns">
               <div class="logo">
                    <a href="#"><img src="images/logo.png" alt="Jottly" /></a>
               </div>
          </div>
+     <div class="thirteen columns">
          <nav>
               <ul>
                    <li><a href="#">Sign In</a></li>
                    <li><a href="#">Sign Up Now</a></li>
               </ul>
          </nav>
+     </div>
     </div>
...
```

In order to meet the full width of our `container`, we must add up to 16 columns. It's not always a necessity, but makes it easier for you to remember how much content you can include in the width of a page. So we wrap the `nav` tag and the nested content in a new `div` with a `class` of 'thirteen columns'. This stretches all content across the full width of the page, filling the full 960 pixels.

Next, we're going to update the text that appears on the header image. In this case, we don't want the content to fill the width of the page.

```html(index.html)
...
-     <h1>An easier way to write &amp; collaborate</h1>
-     <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
+     <div class="container">
+          <div class="nine columns">
+               <h1>An easier way to write &amp; collaborate</h1>
+               <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>			
+          </div>
+     </div>
...
```

With our `h1` and `p` tags, we're going to begin a new `container`. This time, we'll nest a new `div` set at `nine columns`, so it leaves some open space on the right side. When we begin working with the CSS, you'll get a better picture of why we're not filling the full width.

Be sure to end each of those divs to close out the `container`.

Next, we'll add in the grid structure for the input field and submit button.

```html(index.html)
...
-     <input type="text" placeholder="Enter your email address"/>
-     <button type="submit">Sign Up Now</button>
     <div class="container">
          <div class="nine columns">
               <h1>An easier way to write &amp; collaborate</h1>
               <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
+
+               <div class="container">
+                    <div class="row">
+                         <div class="five columns alpha">
+                              <input type="text" placeholder="Enter your email address"/>
+                         </div>
+                         <div class="four columns omega">
+                              <button type="submit">Sign Up Now</button>
+                         </div>
+                    </div>
+               </div>
          </div>
     </div>
...
```

Before the closing `</div` for the `nine columns`, we want to begin a new `container` div. Nested directly under that, we'll add in a new div with a class of `row`. A row helps define nested rows inside containers.

We're going to wrap the input field in a `div` set to five columns. There's an additional class of `alpha`. Within Skeleton, you can define the first column of a row or container to remove the padding and margin from the left side, so the content is flush with the other content directly above it. You'll also notice that the next div is set to `four columns`. Because we've defined our original container and nested div at nine columns, we must add up to that to fill the width of the content. Additionally, we have `omega` as a class in this div. Like `alpha`, it removes padding and margin, but from the right side instead. Alpha being first, and omega being last.

Next, we're going to add the grid structure to the Benefits section.