## Integrating a grid layout

![](http://cl.ly/WGOc/07-header-skeleton.png)

In this checkpoint we'll integrate [Skeleton's grid layout]((http://www.getskeleton.com/#grid)) to improve the presentation of our landing page.

### Container class

A container class defines the width for displaying content. The skeleton.css file in the stylesheets directory defines the container class. Open the file and you'll see that the width is defined as 960 pixels. The 960 pixel page width is comprised of 16 columns. This is important to remember as we integrate the grid with our landing page.

Columns will be used within the container div.

First we'll create a container for the logo and header navigation elements:

```html(index.html)
<!-- Header
================================================== -->
<div id="header">
- <img src="images/logo.png" />
+ <div class="container">
+   <div class="three columns">
+     <div class="logo">
+       <a href="#"><img src="images/logo.png" alt="Jottly" /></a>
+     </div>
+   </div>
    <nav>
      <ul>
        <li><a href="#">Sign In</a></li>
        <li><a href="#">Sign Up Now</a></li>
      </ul>
    </nav>
    <h1>An easier way to write &amp; collaborate</h1>
    <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
    <input type="text" placeholder="Enter your email address"/>
    <button type="submit">Sign Up Now!</button>
+  </div>
</div>
```

The first new div defines the container. We used a nested div to define the number of columns for the logo div, which will be three. We also wrapped the image tag in an anchor tag, so it will be rendered as a link.

Let's update our navigation area:

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
+   <div class="thirteen columns">
      <nav>
        <ul>
          <li><a href="#">Sign In</a></li>
          <li><a href="#">Sign Up Now</a></li>
        </ul>
      </nav>
+   </div>
...
```

We should account for 16 columns to fill the width of our container, so we nested the nav tag within a div class of thirteen columns. This will stretch the contained content across the remaining width of the page.

Next, we'll update the text that appears on the header image. In this case, we don't want the content to fill the width of the page.

```html(index.html)
    <div class="container">
      <div class="three columns">
        <div class="logo">
          <a href="#"><img src="images/logo.png" alt="Jottly" /></a>
        </div>
      </div>
      <div class="thirteen columns">
        <nav>
          <ul>
            <li><a href="#">Sign In</a></li>
            <li><a href="#">Sign Up Now</a></li>
          </ul>
        </nav>
      </div>
    </div>

-   <h1>An easier way to write &amp; collaborate</h1>
-   <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
+   <div class="container">
+     <div class="nine columns">
+     <h1>An easier way to write &amp; collaborate</h1>
+     <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
+    </div>
+  </div>
...
```

We replaced the h1 and paragraph tags with a new container div. We nested another div within the container and set it to nine columns. This will create some open space on the right side of the page. When we begin styling the page, you'll get a better sense of why we're not filling the full width of the page.

Next, we'll add the grid structure for the input field and submit button.

```html(index.html)
    <div class="container">
      <div class="nine columns">
        <h1>An easier way to write &amp; collaborate</h1>
        <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
-       <input type="text" placeholder="Enter your email address"/>
-       <button type="submit">Sign Up Now</button>
+
+       <div class="container">
+         <div class="row">
+           <div class="five columns alpha">
+             <input type="text" placeholder="Enter your email address"/>
+           </div>
+           <div class="four columns omega">
+             <button type="submit">Sign Up Now</button>
+           </div>
+         </div>
+       </div>
      </div>
    </div>
```

We wrapped the input field in a div set to five columns. Notice the additional class of alpha. Skeleton allows us to define the first column of a row or container and remove its padding and margin from the left side. This will make the content flush with content directly above it. To understand why this happens, let's review the box model.

### Box Model
The Box Model defines how HTML elements are laid out. Imagine all HTML elements as boxes on a page. These consist of four parts:

![](https://bloc-global-assets.s3.amazonaws.com/images-design/jottly/css/css-boxmodel.png)

1. **Content**: This is the information (text or images) within HTML tags.
2. **Padding**: This is the area around the content that provides some space. Padding is often part of the background of an element.
3. **Border**: This defines the edge of the HTML element. It encases the padding and content. It can be a stylized border, as in a color and stroke size, or it can be non-stylized, which means it still exists but doesn't have any visual traits.
4. **Margin**: This is the transparent space around an element. Margin creates space between objects without having any traits of the content, padding or border.

All of these items will make up the total calculated width of a HTML element. Let's look at an example to see how this applies:

```css
width:300px;
padding:10px;
border:5px solid black;
margin:10px;
```

![](https://bloc-global-assets.s3.amazonaws.com/images-design/jottly/css/css-boxmodel-math.png)

So, by doing the math, you get 350 pixels. OK, let's get back to it.

You'll notice that the next div is set to four columns. Because we defined the original container and nested div at nine columns, we should account for the full width of the page.

We also used an omega class. Like the alpha class, it removes padding and margin, but from the right side instead of the left.

You can refresh to view the changes you've made.

### Pushing your changes

Push your changes to Github:

```bash(Terminal)
$ git add .
$ git commit -m "Integrated grid system to header and nav sections"
$ git push origin gh-pages
```

Next, we'll add the grid structure to the Benefits section.
