## Downloading Skeleton

![Download Skeleton](http://cl.ly/WEym/01-skeleton.png)

In this checkpoint, we're going to download a simple HTML and CSS framework called [Skeleton](http://www.getskeleton.com/). We'll use this markup to develop the landing page for Jott.ly.
	
### Setting up

You can easily download the source code by clicking on `Download` in the left-hand navigation of the Skeleton site. It will direct you to a button to `Download Skeleton 1.2 from Github`. The files come in a zipped file. Double-click to extract it, and then you'll want to rename the folder `Jottly` and keep it in an easy-to-find location on your machine.

Within that folder, you will see the directory structure for Skeleton, which includes the following:

* `index.html`: This is the main HTML page we will edit.
* `/stylesheets`: This directory/folder holds all of our CSS files.
* `/stylesheets/base.css`: This file contains all of the basic styles for the Skeleton template.
* `/stylesheets/skeleton.css`: This file is strictly the grid that we'll be using.
* `/stylesheets/layout.css`: This doesn't contain any specific styles currently, but will be used for media queries which allow the site to be designed responsively.
* `/images`: This directory/folder holds the images that will be displayed on the site.

### Github

Before going any further, we want to setup a Github repository to store our files. If you don't have a [Github](https://github.com/), sign up for one and create a new repository called `Jottly`.  You will see instructions to push your code to Github.

Before pushing your code to Github, change the path to your `Jottly` folder on your machine using Command Line in Terminal. For instance, if you saved to your desktop, you would enter this:

```bash(Terminal)
$ cd Desktop/Jottly
```

Next follow the instructions to set up your Github repo. 

```bash(Terminal)
$ git init
$ git add .
$ git commit -m "First commit"
$ git remote add origin https://github.com/<user name>/Jottly.git
$ git push -u origin master
```

We will use this repo to host and store your code as you work through the HTML and CSS of the Jott.ly landing page.