## Managing your code

![](https://bloc-books.s3.amazonaws.com/jottly/github.png)

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