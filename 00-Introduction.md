## Introduction to Jott.ly

![Final Jott.ly](http://cl.ly/WFMS/jottly.gif)

Welcome to Jott.ly! In this checkpoint, we'll introduce you to what we plan on building.

Jott.ly is a fictitious SaaS (Software as a Service) web application focused on simplifying collaboration on content. 

The landing page we're going to be building has already been designed. You will be provided with several images to integrate in later on. Your focus will be on completing the HTML and CSS so it looks like the final product displayed above.

Before we get started, let's quickly review what HTML and CSS are, and how each of them are structured. Understanding how to breakdown both HTML and CSS will help you complete this with ease.

### What is HTML?

HTML (HyperText Markup Language) is the markup language browsers use to display web sites. Anything you see rendered in a browser is served up using HTML and CSS - which we'll get into later on.

HTML is written using tags encased in angled brackets (<>), which define content. Typically, a tag begins with a opening tag (<>) and ends with a closing tag (</>). The content goes in between these tags like this:

```html
<tag>Content</tag>
```

Attributes are applied to tags to provide additional information. These fall in line after the name of the tag you are using, like below:

```html
<tag attribute="value">Content</tag>
```

### What is CSS?

CSS (or Cascading Style Sheets) provides a presentation layer to your HTML, defining how elements are displayed and styling using color, font, margins, padding, and page layout.

Before CSS became the norm for designing web sites, most of the web was built using tables. CSS has eased the process for designers and front-end developers, making the web a more beautiful place.

[CSS Zen Garden](http://www.csszengarden.com/) showcases how powerful CSS can be in redefining the look and feel of a single web site of content. Take some time to look at a few examples, like [Dan Mall's Garments](http://www.csszengarden.com/220/), [Trent Walton's Apothecary](http://www.csszengarden.com/218/) and [Elliot Jay Stocks' Screen Filler](http://www.csszengarden.com/217/).

The syntax of CSS is defined by first a `selector`, followed by one or more declarations, which are comprised of a `property` and a `value`. For example:

```CSS
selector {property: value; property: value;}
```

The `property:value;` within curly brackets is the declaration, which ends with a semicolon before starting a new declaration. Typically, to make reading CSS easier, you should put each declaration on a a new line with an indentation, like so:

```CSS
selector {
	property: value;
	property: value;
}
```

Always make sure you remember to end each declaration with the semicolon and close the curly bracket when finished adding all declarations, or it will result in a busted style.

Now that you understand the basics, let's get to coding!