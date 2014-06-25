## Adding Header and Images

![Adding header](http://cl.ly/WFBz/03-header.png)

In this checkpoint, we will add in the images you will need for your Jott.ly landing page along with adding our HTML for the header.

### Adding images to your images directory

Download [this set of images](http://cl.ly/WFEA/Jottly-Images.zip). Extract the ZIP file. Select the images inside the folder and drag them into your `images` folder in your `Jottly` directory.

You should see the following images:

* `action.jpg`
* `app.png`
* `avatar1.jpg`
* `avatar2.jpg`
* `avatar3.jpg`
* `header.jpg`
* `logo.png`
* `small_logo.png`

Don't worry about these for now, as we'll begin adding them into our HTML and CSS to render on the landing page.


### Updating the HTML with your header content

We're going to add the first section (the header) to our landing page using a `div` tag. `Div`, or division, is a block element created to combine other groups of code together.

```html(index.html)
<body>
-
- <h1>Hello world!</h1>
- 
+     <!-- Header
+     ================================================== -->
+     <div id="header">
+     </div>
</body>
</html>
```

Within this `div` tag, we've added the attribute `id`, which identifies a single element on a page. When naming elements, you can choose to give them an `id` or `class`. Once we get to the sections about CSS, we'll discuss the difference between these two in further detail and how to use them properly. For the time being, we've named this `header`, which we'll use when styling the content in our CSS.

> Any time you start a tag, such as `<div>`, it's important to remember to immediately close it using a forward slash, like `</div>`, so you don't end up with unclosed tags. 

Next, we're ready to begin adding content to our header.

```html(index.html)
<div id="header">
+     <img src="images/logo.png" />
</div>
```

Earlier we added several images to our `images` directory. We're going to use one as our logo — `logo.png`. To include this in our HTML, we can add an `img` tag in our HTML, and then it must be sourced (`src`) to where it resides in our directory structure. In this case, the logo is named `logo.png`, and is inside the `images` folder. Since our `index.html` file is on the top level of our directory, you first must point to the folder where your content is located, and then the file name, i.e. `src="images/logo.png"`. If the image fails to show up, it's often because the source path isn't properly written.

> `img` tags don't require a closing tag. You can end it by adding in a forward slash right before the last >, i.e., `/>`.

Next, we'll add in some navigation links. While these won't be connected to any additional pages, it's important to account for any additional pages or views the user may encounter when using a web site. In this case, we're only adding two: sign in and sign up now.

```html(index.html)
<div id="header">
     <img src="images/logo.png" />
+    <nav>
+         <ul>
+              <li><a href="#">Sign In</a></li>
+              <li><a href="#">Sign Up Now</a></li>
+         </ul>
+     </nav>
</div>
```

We started with a `nav` tag, which defines a group of navigation links. Inside of the `nav` tag, we include an unordered list (`ul`). These help build simple lists, and are often used to define navigation links. Nested inside the `ul`, we have two `li`, or list items. Within these, the text is wrapped with an anchor tag, or `a`, which defines a link to another section of content, page or external link. This is determined by the `href="#"`.

> We are using the hashtag (`#`) for our anchor tags because we don't currently have pages they will link to. If you wanted to link to another page, you would replace the hashtag with the name of the file, for example, `href="about.html"`.

Now, let's add in a headline and some paragraph text to explain what Jott.ly is all about.

```html(index.html)
<div id="header">
     <img src="images/logo.png" />
     <nav>
          <ul>
               <li><a href="#">Sign In</a></li>
               <li><a href="#">Sign Up Now</a></li>
          </ul>
     </nav>
+    <h1>An easier way to write &amp; collaborate</h1>
+    <p>Put down the pen and paper. Jott.ly helps you organize your <strong>life, home and office</strong>. It's a simple way to store and share ideas with your loved ones, friends and colleagues.</p>
</div>
```

Headers come in six default size — `h1`, `h2`, `h3`, etc. The `h1` tag should **always** be used as your primary headline on the page, not only for sizing purposes, but also for better SEO (or Search Engine Optimization).

Using the paragraph (`p`) tag, we can include some additional explanation of what Jott.ly is and does. We've selected a portion of this text to **bold** using the `strong` tag. If you wanted some text to appear as italics, you could wrap that text in the `em` tag.

Next, we're going to add in a simple text input field along with a submit button. Eventually, these elements could be used for gathering users' email addresses.

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
+    <input type="text" placeholder="Enter your email address"/>
+    <button type="submit">Sign Up Now</button>
</div>
```

We defined our `input` with a type of `text` so the user can insert content when they add in their email address. There are a number of [input types](http://www.w3schools.com/tags/att_input_type.asp) that could be used. If we wanted to change this to `email`, it would work just the same. The attribute `placeholder` allows you to define the text that appears inside the field before a user enters their information. This can provide some helpful context for the user.

> Inputs are another tag in HTML that don't need a closing `</>` tag, much like images.

Next, we add in a button so that the user can complete the action of signing up. We use the `button` tag, and again, define the type, but this time using `submit`. Wrapped in the tag, we include the text that will appear on the button.

### Pushing your changes

Again, we will push your changes to your Github repo so that we store the latest code.

```bash(Terminal)
$ git add .
$ git commit -m "Added header content and images"
$ git push
```

Now, we have the content set up for our header. We're going to continue going down the page, adding each section and then focus on styling those to get our final product.

 
