## Applying a Grid Layout to the Benefits Section

<center>![](https://bloc-global-assets.s3.amazonaws.com/images-design/blocbooks/jottly/jottlybenefitsgrid.png)</center>

In this checkpoint we'll apply a grid layout to the Benefits section. In the process we'll use a new class that offsets columns. Let's start by creating a new container and nesting the offset div:

```html(index.html)
  <!-- Benefits
  ================================================== -->
  <section class="benefits">
+   <div class="container">
+     <div class="eight columns offset-by-two">
        <h2>What is Jott.ly exactly?</h2>
        <p>Our web application allows you to create documents with real-time editing and collaborating capabilities, while storing content and information to share with others.</p>
+     </div>
      <img src="images/app.png" alt="Jottly's Web Application" />
+   </div>
  </section>
```

The offset on the eight-column div centers its contained content by two columns on either side.

```html(index.html)
  <!-- Benefits
  ================================================== -->
  <section class="benefits">
    <div class="container">
      <div class="eight columns offset-by-two">
        <h2>What is Jott.ly exactly?</h2>
        <p>Our web application allows you to create documents with real-time editing and collaborating capabilities, while storing content and information to share with others.</p>
      </div>
-     <img src="images/app.png" alt="Jottly's Web Application" />
+     <div class="ten columns offset-by-one">
+       <img class="scale-with-grid" src="images/app.png" alt="Jottly's Web Application" />
+     </div>
    </div>
  </section>
```

We wrapped the img tag inside a 10-column div and used an offset to center the contained content. We added the scale-with-grid class to our img tag which allows images to fit to the grid on mobile devices, laptops and large-screen monitors.

Next we'll work on improving the pricing tier layouts.
