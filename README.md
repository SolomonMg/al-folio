# A clean, lightning-fast theme for social scientists
(Forked from '[al-folio](https://alshedivat.github.io/al-folio/)')

## Getting started

For more about how to use Jekyll, check out [this tutorial](https://www.taniarascia.com/make-a-static-website-with-jekyll/).
Why Jekyll? Read this [blog post](https://karpathy.github.io/2014/07/01/switching-to-jekyll/)!

### Installation

Assuming you have a Mac, first install [brew](https://brew.sh/). Install [Ruby](https://www.ruby-lang.org/en/downloads/), gcc, and [Bundler](https://bundler.io/) using brew and [rbenv](https://github.com/rbenv/rbenv):

```bash
brew update
brew install rbenv
brew install ruby-build
brew tap homebrew/dupes
brew install autoconf automake apple-gcc42
```

first fork the theme from `github.com:SolomonMg/
SolomonMg.github.io` to `github.com:<your-username>/<your-repo-name>` and do the following:

```bash
git clone git@github.com:<your-username>/<your-repo-name>.git
cd <your-repo-name>
bundle install
bundle exec jekyll serve
```

## Customizing 
First open `_config.yml` and customize for you. 

Have a look in the `/_pages/` directory. Here you can edit markdown for the actual pages used--about, projects, publications, etc. 

Note that `_pages/about.md` is built to index.html in the published site. There is therefore no need to have a separate index page for the project. If an index page does exist in the root directory then this will prevent `_pages/about.md` from being added to the built site.


Next, open the `_projects/` directory. Name your projects according to the current file naming scheme, and modify as appropriate. 

Now open, `/_posts/` where you can create blogposts. Again, use the current file naming scheme and all will be well.  

Put your pdfs in `/assets/pdf/` and your images in `/assets/img/`. 

If you want to post personal/professional news updates to your website, put them in `/_news/`.  

## Advanced customization
If you want to customize the html layout for any of these pages, edit it in `/_layouts/`. Various html components can also be edited in `/_includes/`. 

If you want to customize the CSS, edit it in `/_sass/`. 

## Saving and deploying

To preview your website run this from the command line: 

```bash
cd <your-repo-name>
/bin/serve
```

When you are at a good stopping place, **commit** your final changes. YOU MUST COMMIT YOUR CHANGES if you don't, you WILL lose work when you deploy. 

```bash
/bin/commit '<informative commit message clearly describing what youve done since your last commit'>
```

This will save (commit) your changes to the `source` branch. You'll deploy to the `master` branch. If you don't understand what that means, don't worry about it too much. You can learn more about branching with git and GitHub using [GitHub's tutorial](https://guides.github.com/activities/hello-world/) or this article from [The New Stack](https://thenewstack.io/dont-mess-with-the-master-working-with-branches-in-git-and-github/). 

I recommend 'pushing' your local changes (commits) to your GitHub repository for tracking purposes: 

```bash
git push
```

Now, you can deploy your website to [GitHub Pages](https://pages.github.com/) by running the deploy script:

```bash
/bin/deploy
```

## Features

#### Collections
This Jekyll theme implements collections to let you break up your work into categories.
The example is divided into news and projects, but easily revamp this into apps, short stories, courses, or whatever your creative work is.

> To do this, edit the collections in the `_config.yml` file, create a corresponding folder, and create a landing page for your collection, similar to `_pages/projects.md`.

Two different layouts are included: the blog layout, for a list of detailed descriptive list of entries, and the projects layout.
The projects layout overlays a descriptive hoverover on a background image.
If no image is provided, the square is auto-filled with the chosen theme color.
Thumbnail sizing is not necessary, as the grid crops images perfectly.

#### Theming
Six beautiful theme colors have been selected to choose from.
The default is purple, but quickly change it by editing `$theme-color` variable in the `_sass/variables.scss` file (line 72).
Other color variables are listed there, as well.

#### Photos
Photo formatting is made simple using rows of a 3-column system.
Make photos 1/3, 2/3, or full width.
Easily create beautiful grids within your blog posts and projects pages:

<p align="center">
  <a href="https://alshedivat.github.io/al-folio/projects/1_project/">
    <img src="assets/img/photos-screenshot.png" width="75%">
  </a>
</p>

#### Code Highlighting
This theme implements Jekyll's built in code syntax highlighting with Pygments.
Just use the liquid tags `{% highlight python %}` and `{% endhighlight %}` to delineate your code:

<p align="center">
  <a href="https://alshedivat.github.io/al-folio/blog/2015/code/">
    <img src="assets/img/code-screenshot.png" width="75%">
  </a>
</p>

## Contributing

Feel free to contribute new features and theme improvements by sending a pull request.
Style improvements and bug fixes are especially welcome.

## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
