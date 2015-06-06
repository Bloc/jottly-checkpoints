## Integrating a Grid Layout

<center>![Grid](https://bloc-global-assets.s3.amazonaws.com/images-design/blocbooks/jottly/jottlyheadergrid.png)</center>

In this checkpoint we'll integrate [Skeleton's grid layout](http://www.getskeleton.com/#grid) to improve the presentation of our landing page.

### Containers

A container class defines the width for displaying content. The skeleton.css file in the stylesheets directory defines the container class. Open the file, search for the container class, and you'll see that the width is defined as 960 pixels. The 960 pixel page width is comprised of 12 columns. This is important to remember as we integrate the grid with our landing page.

First we'll create a container for the logo and header navigation elements:

```html(index.html)
<!-- Header
================================================== -->
<header>
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
+ </div>
  <h1>An easier way to write &amp; collaborate</h1>
  <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
  <input type="email" placeholder="Enter your e-mail address"/>
  <button type="submit">Sign Up Now!</button>
</header>
```

The first new div defines the container. We used a nested div to define the number of columns for the logo div, which will be three. We also wrapped the image tag in an anchor tag, so it will be rendered as a link.

Let's update our navigation area:

```html(index.html)
<!-- Header
================================================== -->
<header>
  <div class="container">
    <div class="three columns">
      <div class="logo">
        <a href="#"><img src="images/logo.png" alt="Jottly" /></a>
      </div>
    </div>
+   <div class="nine columns">
      <nav>
        <ul>
          <li><a href="#">Sign In</a></li>
          <li><a href="#">Sign Up Now</a></li>
        </ul>
      </nav>
+   </div>
...
```

We should account for 12 columns to fill the width of our container, so we nested the nav tag within a div class of 9 columns. This will stretch the contained content across the remaining width of the page.

Next, we'll update the text that appears on the header image. In this case, we don't want the content to fill the width of the page.

```html(index.html)
...
- <h1>An easier way to write &amp; collaborate</h1>
- <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
- <input type="email" placeholder="Enter your e-mail address"/>
- <button type="submit">Sign Up Now</button>
+ <div class="container">
+  <div class="seven columns">
+    <h1>An easier way to to write &amp; collaborate</h1>
+    <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
+    <input type="email" placeholder="Enter your e-mail address"/>
+    <button type="submit">Sign Up Now</button>
+  </div>
+ </div>
...
```

We replaced the h1 and paragraph tags with a new container div. We nested another div within the container and set it to nine columns. This will create some open space on the right side of the page. When we begin styling the page, you'll get a better sense of why we're not filling the full width of the page.

Next, we'll add the grid structure for the input field and submit button.

```html(index.html)
<div class="container">
  <div class="seven columns">
    <h1>An easier way to to write &amp; collaborate</h1>
    <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
-   <input type="text" placeholder="Enter your email address"/>
-   <button type="submit">Sign Up Now</button>
+   <div class="row">
+     <div class="eight columns alpha">
+       <input type="email" placeholder="Enter your e-mail address"/>
+     </div>
+     <div class="four columns omega">
+       <button type="submit">Sign Up Now</button>
+     </div>
+   </div>
  </div>
</div>
```

We wrapped the input field in a div set to five columns. Notice the additional class of alpha. Skeleton allows us to define the first column of a row or container and remove its padding and margin from the left side. This will make the content flush with content directly above it. To understand why this happens, let's review the box model.

### Box Model
The Box Model explains how HTML elements are positioned. Imagine HTML elements as boxes on a page. The boxes consist of four parts:

![](https://bloc-global-assets.s3.amazonaws.com/images-design/jottly/css/css-boxmodel.png)

1. **Content**: the information (text or images) within HTML tags.
2. **Padding**: the area around the content that provides space. Padding is often part of the background of an element.
3. **Border**: defines the edge of the HTML element. It encases the padding and content.
4. **Margin**: the transparent space around an element. Margins create space between objects without having any traits of the content, padding or border.

All of these items comprise the total calculated dimensions of an HTML element. Let's look at an example:

```css
width:300px;
padding:10px;
border:5px solid black;
margin:10px;
```

<center>![](https://bloc-global-assets.s3.amazonaws.com/images-design/jottly/css/css-boxmodel-math.png)</center>

The width of this box equals 350 pixels, because we add each component of the box together.

Let's get back to our container:

```html(index.html)
<div class="four columns omega">
  <button type="submit">Sign Up Now</button>
</div>
```

You'll notice that the div is set to four columns. Because we defined the original container and nested div at nine columns, we should account for the full width of the page. We also used an omega class. Like the alpha class, it removes padding and margin, but from the right side instead of the left.

You can refresh your browser to view the changes.

Next, we'll apply a grid layout to the Benefits section.
