## Managing your code

<center>![GitHub](https://bloc-books.s3.amazonaws.com/jottly/github.png)</center>

### Git

Whether you're coding alone, or contributing to a project with others, you need a way to manage your code. Fortunately, there's a process called **version control**. As defined by [Scott Chacon](http://scottchacon.com/) in [Pro Git](http://git-scm.com/book):

> Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later.

Here's an excerpt from the [Pro Git book](http://git-scm.com/book) that explains how Git solves version control at a high level:

> ...Git thinks of its data more like a set of snapshots of a mini file system. Every time you commit, or save the state of your project in Git, it basically takes a picture of what all your files look like at that moment and stores a reference to that snapshot. To be efficient, if files have not changed, Git doesn’t store the file again, just a link to the previous identical file it has already stored. Git thinks about its data like this:

<center>![Git Basics](http://bloc-global-assets.s3.amazonaws.com/screencaps/git_basics.png)</center>

Git is popular because of its distributed and collaborative nature. This means that you don't need to be online to use Git, but it's still easy to collaborate with large teams on the same project. When you need to collaborate with other people or services, you can push your code to a Git server, like [GitHub](https://github.com/).

> You'll need to [download and install Git](http://git-scm.com/downloads) to work with GitHub and deploy Jottly, so install Git before moving on. If you are using a Mac, you may get blocked by Mac's security settings. Not to worry, Git is a safe and trusted resource, and used by most developers and designers today. Just update your security settings as prescribed to complete the installation.

You do not need to explicitly launch Git as an application. Once it's installed, you'll be able to access its functionality on the command line, as we'll detail below.

### GitHub

[GitHub](http://github.com) is a service that allows you to host and store your code on the web. It also includes social features for sharing and collaborating on projects. For most developers, GitHub profiles showcase much of the development work they've done. Companies often place more importance on a prospective employee's GitHub profile than their resume. GitHub offers [freemium pricing](https://github.com/plans), so register for a free account now.

Once you have a GitHub account, [create a GitHub repository](https://help.github.com/articles/create-a-repo) named **Jottly**. After creating a new repo you will see instructions for "pushing" code from your computer to GitHub.

Before pushing your code to GitHub, change the path of your working directory using the Command Line. For example, if you moved your **Jottly** folder to a directory named **projects**, you would enter the following on your command line:

> The command line can be accessed using the "Terminal" app on Mac OS X, or the "CMD" app on Windows. On a Mac, you can type "Terminal" into Spotlight. On a Windows computer, type "CMD" into the Run prompt from the Start menu.

```bash(Terminal)
$ cd projects/Jottly
```

Follow the instructions in GitHub to initialize your repo:

```bash(Terminal)
$ git init
$ git add .
$ git commit -m "First commit"
$ git remote add origin https://github.com/<user name>/Jottly.git
$ git push -u origin master
```

In the next checkpoint, we'll deploy Jottly using GitHub Pages so you can view the results online with a public URL.
