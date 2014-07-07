## Downloading Skeleton

![Download Skeleton](http://cl.ly/WEym/01-skeleton.png)

In this checkpoint we'll download a simple HTML and CSS framework named [Skeleton](http://www.getskeleton.com/) and use it to develop the landing page for Jottly.

### Install Skeleton

![Downloading Skeleton](http://cl.ly/WKiD/download-skeleton.gif)

Download the source code by clicking on the **Download** link in the left-hand navigation of the Skeleton site. Click the button labeled **Download Skeleton 1.2 from Github**. Find the downloaded file named **dhg-Skeleton-7ab6820.tar.gz** and double-click to extract it. Rename the folder to **Jottly** and move it to an easy-to-find location on your machine.

> We suggest creating a "code" or "projects" directory to keep projects like Jottly

Within the **Jottly** folder, you will see the directory structure for Skeleton, which includes the following:

* `index.html`: This is the main HTML page we will edit.
* `/stylesheets`: This directory holds all of our CSS files.
* `/stylesheets/base.css`: This file contains all of the basic styles for the Skeleton template.
* `/stylesheets/skeleton.css`: This file is the grid that we'll be using.
* `/stylesheets/layout.css`: This doesn't contain any specific styles yet, but will be used for media queries which allow the site to be designed responsively.
* `/images`: This directory holds the images that will be displayed on the site.

### Github

[Github](http://github.com) is a service that allows you to host and store your code on the web. It also includes social features for sharing and collaborating on projects. For most developers, Github profiles showcase much of the development work they've done. Companies often place more importance on a prospective employee's Github profile than their resume. Github offers [freemium pricing](https://github.com/plans), so register for a free account now.

Once you have a Github account, [create a Github repository](https://help.github.com/articles/create-a-repo) named **Jottly**. After creating a new repo you will see instructions for "pushing" code from your computer to Github.

> You'll need to [download and install Git](http://git-scm.com/downloads) to work with Github. Install Git before moving on.

Before pushing your code to Github, change the path of your working directory using the Command Line. For example, if you moved your **Jottly** folder to a directory named **projects**, you would enter:

```bash(Terminal)
$ cd projects/Jottly
```

Follow the instructions in Github to initialize your repo:

```bash(Terminal)
$ git init
$ git add .
$ git commit -m "First commit"
$ git remote add origin https://github.com/<user name>/Jottly.git
$ git push -u origin master
```

In the next checkpoint, we'll deploy Jottly using Github Pages so you can view the results online with a public URL.
