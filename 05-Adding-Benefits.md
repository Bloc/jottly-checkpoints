## Adding Benefits and Pricing

![Benefits](http://cl.ly/WEu8/04-benefits.png)

In this checkpoint, we will be adding two more sections to our page: Benefits and Pricing. The first contains some simple HTML, while the latter is more complex in structure, which we'll break down and explain thoroughly.

### Benefits

After the closing `</div>` for your header, begin by adding a comment to define where your new section 'Benefits' begins. 

> You can make a comment in HTML by including an exclamation point and two dashes after the first bracket, like `<!-- Text goes here -->`. But be sure to close it by including two dashes before the last bracket. Commenting makes locating content and sections much easier.

Again, we'll define this `div` with an `id`, this time named `benefits`. 

```html(index.html)
...
</div>
+	<!-- Benefits
+	================================================== -->
+	<div id="benefits">
+	</div>
```

Next, we're going to add some simple content to provide some additional details and a screenshot of the Jott.ly application.

```html(index.html)
...
<!-- Benefits
================================================== -->
<div id="benefits">
+      <h2>What is Jott.ly exactly?</h2>
+      <p>Our web application allows you to create documents with real-time editing and collaborating capabilities, while storing content and information to share with others.</p>
</div>
```

Because we already used an `h1`, we're going to use the next header size — `h2`. We also include another `p` tag and insert text.

```html(index.html)
...
<!-- Benefits
================================================== -->
<div id="benefits">
      <h2>What is Jott.ly exactly?</h2>
      <p>Our web application allows you to create documents with real-time editing and collaborating capabilities, while storing content and information to share with others.</p>
+		
+      <img src="images/app.png" alt="Jottly's Web Application" />
</div>
```

The last part of this section is the image of the web application, so users can see what the app looks like. Using the `img`, we source our image inside the `images` folder and select the `app.png` file.

Next, we're going to dive into a much more complex HTML structure to produce the code to display pricing tiers for the Jott.ly application.

### Pricing Tiers

![Pricing](http://cl.ly/WFh1/04-pricing.png)

At the end of your closing `</div>` tag for benefits, you can again create a new comment and `div` with an `id` of 'pricing' for this new section.

```html(index.html)
...
</div>
+	<!-- Pricing
+	================================================== -->
+	<div id="pricing">
+	</div>
```

We're going to use another `h2` for this section header, along with including some additional `p` text to explain our pricing tiers.

```html(index.html)
...
<!-- Pricing
================================================== -->
<div id="pricing">
+     <h2>How much will it cost me?</h2>
+     <p>It’s rather inexpensive to use Jott.ly’s suite of tools compared to several other services out there. We have several options to fit your budget and needs:</p>
</div>
```

Now, we're going to jump into adding in our price boxes that have a title, price, list of features and a button to select the respective plan. We have three different pricing tiers, so we'll start with the first one.

```html(index.html)
<!-- Pricing
================================================== -->
<div id="pricing">
     <h2>How much will it cost me?</h2>
     <p>It’s rather inexpensive to use Jott.ly’s suite of tools compared to several other services out there. We have several options to fit your budget and needs:</p>
+
+    <div class="pricebox">
+    </div>
</div>
```

Before doing anything else, we want to drop in a `div` with a class. In this case, we've opted to use a `class` attribute because we'll replicate the content of this div multiple times on this page, but want the same styling across each of them. We've created a `div` with the class of `pricebox`. 

Next, we're going to add in a new header, price and some additional text to explain how much per user, per month.

```html(index.html)
<!-- Pricing
================================================== -->
<div id="pricing">
     <h2>How much will it cost me?</h2>
     <p>It’s rather inexpensive to use Jott.ly’s suite of tools compared to several other services out there. We have several options to fit your budget and needs:</p>

     <div class="pricebox">
+          <h3>Individuals &amp; Family</h3>
+          <h4>$2</h4>
+          <p>per month/per user</p>
     </div>
</div>
```

Using hierarchy in HTML markup is a good thing to remember. In this case, we've used `h1` and a few `h2`s earlier on our page. For our header on each individual price box, we're going to opt to use `h3` and then an `h4` for the price. After that, we include a paragraph tag for some additional content.

Next, we have a list of features to include.

```html(index.html)
<!-- Pricing
================================================== -->
<div id="pricing">
     <h2>How much will it cost me?</h2>
     <p>It’s rather inexpensive to use Jott.ly’s suite of tools compared to several other services out there. We have several options to fit your budget and needs:</p>

     <div class="pricebox">
          <h3>Individuals &amp; Family</h3>
          <h4>$2</h4>
          <p>per month/per user</p>
+         <ul>
+              <li>Unlimited notes</li>
+              <li>Unlimited members</li>
+              <li><strong>2GB</strong> of storage</li>
+         </ul>
+         <button>Select this plan</button>
     </div>
</div>
```

Using an unordered list, we can create three list items. As you see in the first list item, we've included the `strong` tag to **bold** the text to place some emphasis on it.

The last piece of this first box is the button, which is simply text wrapped inside a `button` tag. We'll style this later on.

Next, we need to replicate this content for two additional boxes. The easiest way to accomplish this is to grab all of the code from `<div class="pricebox"` to its closing `</div>`, copy and paste it twice below.

```html(index.html)
<!-- Pricing
================================================== -->
<div id="pricing">
     <h2>How much will it cost me?</h2>
     <p>It’s rather inexpensive to use Jott.ly’s suite of tools compared to several other services out there. We have several options to fit your budget and needs:</p>

     <div class="pricebox">
          <h3>Individuals &amp; Family</h3>
          <h4>$2</h4>
          <p>per month/per user</p>
          <ul>
               <li>Unlimited notes</li>
               <li>Unlimited members</li>
               <li><strong>2GB</strong> of storage</li>
          </ul>
          <button>Select this plan</button>
     </div>   
+
+    <div class="pricebox">
+        <h3>Small Businesses</h3>
+        <h4>$5</h4>
+        <p>per month/per user</p>
+        <ul>
+            <li>Unlimited notes</li>
+            <li>Unlimited members</li>
+            <li><strong>15GB</strong> of storage</li>
+            <li>Real-time collaboration</li>
+        </ul>
+        <button>Select this plan</button>
+    </div>
+
+    <div class="pricebox">
+        <h3>Enterprise</h3>
+        <h4>$8</h4>
+        <p>per month/per user</p>
+        <ul>
+            <li>Unlimited notes</li>
+            <li>Unlimited members</li>
+            <li><strong>Unlimited</strong> of storage</li>
+            <li>Real-time collaboration</li>
+        </ul>
+        <button>Select this plan</button>
+    </div>
</div>
```

Before this can be finished though, you must change the header of each of the additional price boxes, the cost and each of the new ones have an additional list item.

Once you complete these steps, you will see three different headers displaying price boxes for 'Individuals & Family', 'Small Businesses', and 'Enterprise'.

Next, we're going to move onto building out our testimonials using the `blockquote` tag.