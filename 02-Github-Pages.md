## Deploying on Github Pages

![](http://cl.ly/WHfi/02-github-pages.png)

In this checkpoint, we'll review how to get your code live online using Github Pages. With your code stored on Github, it allows you to host a live, static site for free.

### Pushing to a new branch

You've already pushed your code to the `master` branch in your Github repository. However, we want to be able to view more than just the source code.

[Github Pages](https://pages.github.com) allows you to host your static websites for free. Open up Terminal and type in the following commands:

```bash(Terminal)
$ git checkout --orphan gh-pages
$ git add .
$ git commit -m "Adding files to gh-pages"
$ git push origin gh-pages
```

The first line here is setting up the new branch called `gh-pages`. Github reads this new branch, and automatically sets up a new URL for you to access the live site.

You will be able to view it at http://**username**.github.io/**repository-name**. If you have trouble locating the URL, you can click on Settings in the right-hand navigation on the repository page on Github.com, and the URL is listed under the section titled 'GitHub Pages'.

> It could take up to 10 minutes for your page to display. The URL will be visible in your settings if you set it up properly.

Next, we're going to begin editing the content of our website. 