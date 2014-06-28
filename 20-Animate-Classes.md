## Updating HTML to include Animate classes

![Animation](http://cl.ly/WGmd/jottly-animate1.gif)

In this checkpoint, we're going to add a subtle animation using Animate.css to our header.

Since we've already added in the stylesheet, we can simply tag our HTML with the various classes so that the animation shown above works.

```html(index.html)
<!-- Header	================================================== -->
-	<div id="header">
+	<div id="header" class="animated fadeInDown">
```

For our `header` div, we're going to add a new attribute of `class` and tag it with `animated`. This will initiate the animation to occur. Next we add a space and then `fadeInDown` to the class. This will finish out the animation for the entire header element.

Next, we're going to add the same classes to the text within the header. Our next lesson will show you why we've opted to add the classes again.

```html(index.html)
-	<div class="nine columns headertext">
+	<div class="nine columns headertext animated fadeInDown">
```

So where our 9-column `headertext` appears in our HTML, we add the same classes of `animated fadeInDown` to it. 

And that's it! We're ready to take the last step.