## Deploying on Github Pages

![Github Pages](http://cl.ly/WHfi/02-github-pages.png)

In this checkpoint we'll deploy Jottly using [Github Pages](https://pages.github.com). Github Pages provides free hosting for static web pages.

### Deploying Jottly

You've already pushed your code to the master branch in your Github repository. However, we want to be able to view more than just the source code; we want to see a live web page as well.

Type the following commands on your command line:

```bash(Terminal)
$ git checkout --orphan gh-pages
$ git add .
$ git commit -m "Adding files to gh-pages"
$ git push origin gh-pages
```

The first line creates a new branch named gh-pages. Github reads this new branch and  creates a new URL for the repo.

You'll be able to view Jottly at: "http://<username>.github.io/<repository-name>". If you have trouble locating the URL, you can click on **Settings** in the right-hand navigation on the repository page - the URL is listed under the section titled **GitHub Pages**.

![Github Pages](http://cl.ly/WLni/jottly-github.gif)

> It might take up to 10 minutes for your page to display after the initial deploy.

Next, we'll start to edit Jottly's content.
