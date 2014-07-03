## Adding Benefits and Pricing

![Benefits](http://cl.ly/WEu8/04-benefits.png)

In this checkpoint we'll be adding two new sections to our landing page: Benefits and Pricing. The Benefits section will be relatively simple, though the Pricing section will require a more complex HTML structure. We'll breakdown the new concepts thoroughly.

### Benefits

After the closing header `</div>` add a comment to define where the Benefits section begins. We'll define this div with an id named header:

```html(index.html)
...
</div>
+ <!-- Benefits
+ ================================================== -->
+ <div id="benefits">
+ </div>
```

> You can make a comment in HTML by including an exclamation point and two dashes after the first bracket: `<!-- Text goes here -->`. Be sure to close it by including two dashes before the last bracket. Commenting can make locating content and sections much easier.

Next, we'll add some simple content to provide details and a screenshot of the Jottly application:

```html(index.html)
...
<!-- Benefits
================================================== -->
<div id="benefits">
+  <h2>What is Jott.ly exactly?</h2>
+  <p>Our web application allows you to create documents with real-time editing and collaborating capabilities, while storing content and information to share with others.</p>
</div>
```

We've already used the h1 tag on our page, so we used the next header size: h2. We also included another paragraph tag with content.

Let's add an image:

```html(index.html)
...
<!-- Benefits
================================================== -->
<div id="benefits">
  <h2>What is Jott.ly exactly?</h2>
  <p>Our web application allows you to create documents with real-time editing and collaborating capabilities, while storing content and information to share with others.</p>
+
+ <img src="images/app.png" alt="Jottly's Web Application" />
</div>
```

The last part of this section is the image of the web application, so users can see what the app looks like. Using the image tag, we source our image inside the images folder and select the app.png file.

Next, we'll explore a more complex HTML structure to produce pricing tiers.

### Pricing Tiers

![Pricing](http://cl.ly/WFh1/04-pricing.png)

At the end of the closing `</div>` tag for benefits, create a new div with an id named pricing:

```html(index.html)
...
</div>
+	<!-- Pricing
+	================================================== -->
+ <div id="pricing">
+ </div>
```

We'll use another h2 for this section header and include paragraph text to explain our pricing tiers.

```html(index.html)
...
<!-- Pricing
================================================== -->
<div id="pricing">
+ <h2>How much will it cost me?</h2>
+ <p>It’s rather inexpensive to use Jott.ly’s suite of tools compared to several other services out there. We have several options to fit your budget and needs:</p>
</div>
```

Let's add price areas that have a title, price, list of features and a button to select the plan. We have three different pricing tiers, so we'll start with the first one.

```html(index.html)
<!-- Pricing
================================================== -->
<div id="pricing">
  <h2>How much will it cost me?</h2>
  <p>It’s rather inexpensive to use Jott.ly’s suite of tools compared to several other services out there. We have several options to fit your budget and needs:</p>
+
+ <div class="pricebox">
+ </div>
</div>
```

Notice that we opted to use a class attribute for the pricebox div. Since we have three pricing tiers we'll need to replicate the styling for each. That is, when an element's style is unique, it's appropriate to use an id. When we have to reuse the styling for an element, we need to use a class.

Next, we'll add a new header, price and some additional text to explain how much Jottly costs per user and per month:

```html(index.html)
<!-- Pricing
================================================== -->
<div id="pricing">
  <h2>How much will it cost me?</h2>
  <p>It’s rather inexpensive to use Jott.ly’s suite of tools compared to several other services out there. We have several options to fit your budget and needs:</p>

  <div class="pricebox">
+   <h3>Individuals &amp; Family</h3>
+   <h4>$2</h4>
+   <p>per month/per user</p>
  </div>
</div>
```

When creating HTML structure it's important to be mindful of hierarchy. We've used h1 and a few h2's earlier on our page. For the header on each individual price box, we used an h3 and h4 to keep our content in the overall context of the landing page. We also included a paragraph tag with additional content.

Let's include our list of features:

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
+   <ul>
+     <li>Unlimited notes</li>
+     <li>Unlimited members</li>
+     <li><strong>2GB</strong> of storage</li>
+   </ul>
+   <button>Select this plan</button>
  </div>
</div>
```

Using an unordered list, we created three list items to represent features. We also included a button so users can select the plan.

Next, we need to replicate this content for two additional boxes. The easiest way to accomplish this is to copy the code from `<div class="pricebox">` to its closing `</div>`, and paste it twice below. Replace the headers and features as stated:

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
+ <div class="pricebox">
+   <h3>Small Businesses</h3>
+   <h4>$5</h4>
+   <p>per month/per user</p>
+   <ul>
+     <li>Unlimited notes</li>
+     <li>Unlimited members</li>
+     <li><strong>15GB</strong> of storage</li>
+     <li>Real-time collaboration</li>
+   </ul>
+   <button>Select this plan</button>
+ </div>
+
+ <div class="pricebox">
+   <h3>Enterprise</h3>
+   <h4>$8</h4>
+   <p>per month/per user</p>
+   <ul>
+     <li>Unlimited notes</li>
+     <li>Unlimited members</li>
+     <li><strong>Unlimited</strong> storage</li>
+     <li>Real-time collaboration</li>
+   </ul>
+   <button>Select this plan</button>
+ </div>
</div>
```

Our landing page now has three different headers, displaying price boxes for 'Individuals & Family', 'Small Businesses', and 'Enterprise'.

Refresh your browser window to view all of the changes you've made.

### Pushing your changes

Push your changes to Github:

```bash(Terminal)
$ git add .
$ git commit -m "Added benefits and pricing"
$ git push origin gh-pages
```

Next, we'll create a testimonials section using the blockquote tag.
