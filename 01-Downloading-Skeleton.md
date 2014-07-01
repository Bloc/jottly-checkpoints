## Downloading Skeleton

![Download Skeleton](http://cl.ly/WEym/01-skeleton.png)

In this checkpoint we'll download a simple HTML and CSS framework named [Skeleton](http://www.getskeleton.com/) and use it to develop the landing page for Jott.ly.

### Up and running

![Downloading Skeleton](http://cl.ly/WKiD/download-skeleton.gif)

Download the source code by clicking on the **Download** link in the left-hand navigation of the Skeleton site. Click the button labeled **Download Skeleton 1.2 from Github**. Find the downloaded file named **dhg-Skeleton-7ab6820.tar.gz** and double-click to extract it. Rename the folder to **Jottly** and move it to an easy-to-find location on your machine.

> We suggest creating a "code" or "projects" directory to store projects like Jott.ly

Within the **Jottly** folder, you will see the directory structure for Skeleton, which includes the following:

* `index.html`: This is the main HTML page we will edit.
* `/stylesheets`: This directory holds all of our CSS files.
* `/stylesheets/base.css`: This file contains all of the basic styles for the Skeleton template.
* `/stylesheets/skeleton.css`: This file is the grid that we'll be using.
* `/stylesheets/layout.css`: This doesn't contain any specific styles yet, but will be used for media queries which allow the site to be designed responsively.
* `/images`: This directory holds the images that will be displayed on the site.

### Github

Before going any further, we'll setup a Github repository to store our files. If you don't have a [Github](https://github.com/) account, sign up and create a new repository named **Jottly**. You will see instructions to initialize your repo and push your code to Github.

> You'll need to [download and install Git](http://git-scm.com/downloads) to work with Github.

Before pushing your code to Github, change the path of your working directory using the Command Line. For example, if you moved your **Jottly** folder to a directory named **code**, you would enter:

```bash(Terminal)
$ cd code/Jottly
```

Follow the instructions in Github to intialize your repo:

```bash(Terminal)
$ git init
$ git add .
$ git commit -m "First commit"
$ git remote add origin https://github.com/<user name>/Jottly.git
$ git push -u origin master
```

In the next checkpoint, we'll deploy Jottly using Github Pages so you can view the results online with a public URL.
