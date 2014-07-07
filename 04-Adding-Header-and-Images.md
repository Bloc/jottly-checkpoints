## Adding a Header and Images

![Adding header](http://cl.ly/WFBz/03-header.png)

In this checkpoint we'll add images to the Jottly landing page and create a new HTML header.

### Download Jottly images

Download [this set of images](http://cl.ly/WFEA/Jottly-Images.zip). Extract the ZIP file and move the images inside the downloaded folder into the Jottly images folder.

You should have the following files in Jottly/images:

* action.jpg
* app.png
* avatar1.jpg
* avatar2.jpg
* avatar3.jpg
* header.jpg
* logo.png
* small_logo.png

### Update the header

We'll add the first section - the header - to our landing page using a div tag. A div, or division, is an HTML element used to define content or a group of elements.

```html(index.html)
<body>
-
- <h1>Hello world!</h1>
-
+ <!-- Header
+ ================================================== -->
+ <div id="header">
+ </div>
</body>
</html>
```

Within this div tag, we've added an attribute id, which identifies a single element on a page. When naming elements, you can choose to give them an id or class. As we learn more about CSS, we'll discuss the differences between classes and ids.

We've given our div an id named header, which we'll use for styling the header content. Let's add an image to our header:

```html(index.html)
<div id="header">
+ <img src="images/logo.png" />
</div>
```

We use an img tag to include the logo.png file we downloaded earlier. The img must be sourced (src) to where it resides in our directory structure. In this case, the logo is named logo.png, and is inside the images folder. Since our index.html file is on the top level of our directory, we must point to the folder where the content is located, and then the file name. If an image fails to render, it's often because the source path isn't properly defined.

> img tags don't require separate closing tags. They can be closed by adding a forward slash right the last ">".

Next, we'll add placeholder navigation links. These links won't be connected to additional pages at this point. In this case, we'll add two: "Sign In" and "Sign Up Now":

```html(index.html)
<div id="header">
  <img src="images/logo.png" />
+  <nav>
+    <ul>
+      <li><a href="#">Sign In</a></li>
+      <li><a href="#">Sign Up Now</a></li>
+    </ul>
+  </nav>
</div>
```

We started with a nav tag, which defines a group of navigation links. Inside the nav tag, we include an unordered list (ul). These elements are used for building simple lists, and are often used to define navigation links. Nested inside the unordered list, we have two li tags, or list items. Within these elements, the text is wrapped with an anchor tag (a), which defines a link to a different location. The destination of the link is determined by the href.

> We are using the hashtag (#) for our href because we don't currently have pages to link to. If you wanted to link to another page, you would replace the hashtag with the name of the file, e.g. href="about.html".

Let's add a headline and some paragraph text to explain what Jottly is all about:

```html(index.html)
<div id="header">
  <img src="images/logo.png" />
  <nav>
    <ul>
      <li><a href="#">Sign In</a></li>
      <li><a href="#">Sign Up Now</a></li>
    </ul>
  </nav>
+ <h1>An easier way to write &amp; collaborate</h1>
+ <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
</div>
```

Headers come in six default sizes — h1, h2, h3, etc. The h1 tag should **always** be used as the primary headline on the page, not only for sizing purposes, but also for better search engine optimization (SEO).

Using the paragraph (p) tag, we explain what Jottly is and does. We've selected a portion of this text to **bold** using the strong tag. If you wanted some text to be italicized, you would wrap that text in the <em> tag.

Next, we'll add a simple text input field along with a submit button. Eventually, these elements could be used for gathering email addresses:

```html(index.html)
<div id="header">
  <img src="images/logo.png" />
    <nav>
      <ul>
        <li><a href="#">Sign In</a></li>
        <li><a href="#">Sign Up Now</a></li>
      </ul>
    </nav>
    <h1>An easier way to write &amp; collaborate</h1>
    <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
+   <input type="text" placeholder="Enter your email address"/>
+   <button type="submit">Sign Up Now</button>
</div>
```

We defined our input with a type of text so a user can enter their email address. There are a number of [input types](http://www.w3schools.com/tags/att_input_type.asp). We could also change this field type to "email". The attribute placeholder allows us to define the text that appears inside the field before a user enters their information. This provides helpful context for the user.

> Inputs are another tag in HTML that don't need a closing </> tag, like image tags.

We also added a "sign up" button. We used the button tag and defined the type as "submit". We included the text that will appear on the button inside of the tag.

Refresh your browser to view the changes.

### Github

Push your changes to Github:

```bash(Terminal)
$ git add .
$ git commit -m "Added header content and images"
$ git push origin gh-pages
```
