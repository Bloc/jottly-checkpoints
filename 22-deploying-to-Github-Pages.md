## Deploying on GitHub Pages

<center>![GitHub Pages](https://bloc-books.s3.amazonaws.com/jottly/02-github-pages.png)</center>

In this checkpoint we'll deploy Jottly using [GitHub Pages](https://pages.github.com). GitHub Pages provides free hosting for static web pages.

### Deploying Jottly

You've already pushed your code to the master branch in your GitHub repository. However, we want to be able to view more than just the source code; we want to see a live web page as well.

Type the following commands on your command line:

```bash(Terminal)
$ git checkout --orphan gh-pages
$ git add .
$ git commit -m "Adding files to gh-pages"
$ git push origin gh-pages
```

The first line creates a new branch named gh-pages. GitHub will read this new branch and create a new URL for the repo.

You'll be able to view Jottly at:

```
http://<username>.GitHub.io/<repository-name>
```

If you have trouble locating the URL, you can click on **Settings** in the right-hand navigation on the repository page - the URL is listed under the section titled **GitHub Pages**.

![GitHub Pages](https://bloc-books.s3.amazonaws.com/jottly/jottly-GitHub.gif)

> It might take up to 10 minutes for your page to display after the initial deploy.

### That's all folks!

Congratulations! You've completed your first landing page and learned a lot about HTML, CSS and how to deploy your site in the process. Jottly is now ready to accept customers, once you've created the actual product :)

### But wait, there's more

Want to learn more? [Build a Tetris app for iOS](https://www.bloc.io/tutorials/swiftris-build-your-first-ios-game-with-swift), using the new **Swift programming language** from Apple. We'll show you how to build a killer game from scratch! 

Or perhaps you'd like to design a [cool music app website](http://bloc-jams.webflow.com/)... with NO code! How is this possible? Check out our [Webflow tutorial](https://www.bloc.io/tutorials/webflow-tutorial-design-responsive-sites-with-webflow) to find out.

If you enjoyed this book, please share it with your friends and followers.
