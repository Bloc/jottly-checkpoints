## Deploying on Github Pages

![](http://cl.ly/WHfi/02-github-pages.png)

In this checkpoint we'll deploy Jottly using [Github Pages](https://pages.github.com). Github Pages provides free hosting for static web pages.

### Pushing to a new branch

You've already pushed your code to the master branch in your Github repository. However, we want to be able to view more than just the source code.

Type the following commands on your command line:

```bash(Terminal)
$ git checkout --orphan gh-pages
$ git add .
$ git commit -m "Adding files to gh-pages"
$ git push origin gh-pages
```

The first line creates a new branch named gh-pages. Github reads this new branch and  creates a new URL for the code.

You will be able to view Jottly at http://username.github.io/repository-name. If you have trouble locating the URL, you can click on Settings in the right-hand navigation on the repository page on Github.com, and the URL is listed under the section titled 'GitHub Pages'.

![Github Pages](http://cl.ly/WLni/jottly-github.gif)

> It could take up to 10 minutes for your page to display.

Next, we'll edit Jottly's content.
