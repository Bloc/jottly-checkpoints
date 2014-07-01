## Adding Animate.css

![Animate CSS](http://cl.ly/WIc5/19-animate.png)

In this checkpoint, we're going to download and add [Animate.css](http://daneden.github.io/animate.css/) to our source code.

[Animate.css](https://raw.github.com/daneden/animate.css/master/animate.css) was created by [Dan Eden](http://daneden.me/) and made open for people to use in their projects.

First, go ahead and [download](https://raw.github.com/daneden/animate.css/master/animate.css) the CSS file and copy and paste it into your `stylesheets` folder. 

The last thing we need to do is link it up in our HTML.

```html(index.html)
 	<link rel="stylesheet" href="stylesheets/base.css">
  	<link rel="stylesheet" href="stylesheets/skeleton.css">
  	<link rel="stylesheet" href="stylesheets/layout.css">
 +	<link rel="stylesheet" href="stylesheets/animate.css">
  ...
```

Directly after where your current three CSS files are linked, you can add in the file located at `stylesheets/animate.css`. This will allow you to tag the animations via classes to the HTML elements we want to manipulate in the next two lessons.