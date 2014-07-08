## Introduction to Jott.ly

![Final Jottly](https://bloc-books.s3.amazonaws.com/jottly/jottly.gif)

Jottly is a fictitious SaaS (Software as a Service) web application focused on simplifying content collaboration. In this book you'll learn how to build the web page shown above, using HTML and CSS.

Before we get started, we'll briefly review HTML and CSS. Understanding how to breakdown HTML and CSS will help you design apps like Jottly with ease.

### HTML

HTML (HyperText Markup Language) is the markup language browsers use to render web sites. Regardless of the programming language used to build the application, its information is ultimately translated to HTML before appearing in a browser.

HTML is written using tags encased in angled brackets (`<>`), which define content. A tag is usually opened (`<>`) and closed (`</>`) around content. Content is written between tags like this:

```html
<tag>Content</tag>
```

Attributes are applied to tags to provide additional information. Attributes are added after the name of the tag:

```html
<tag attribute="value">Content</tag>
```

### CSS

CSS (Cascading Style Sheets) provides a presentation layer for HTML. CSS defines how HTML elements are styled and positioned.

[CSS Zen Garden](http://www.csszengarden.com/) showcases how powerful CSS can be in defining the look and feel of web site of content. Take some time to look at a few examples, like [Dan Mall's Garments](http://www.csszengarden.com/220/), [Trent Walton's Apothecary](http://www.csszengarden.com/218/) and [Elliot Jay Stocks' Screen Filler](http://www.csszengarden.com/217/).

CSS syntax is comprised of selectors, properties and values. For example:

```css
selector {property: value; property: value;}
```

The `property:value;` within curly brackets is the declaration and ends with a semicolon before the next declaration begins. Well-written CSS should state each declaration on a new line with a double-spaced indentation:

```css
selector {
  property: value;
  property: value;
}
```

Now that you understand the basics, let's get to coding!
