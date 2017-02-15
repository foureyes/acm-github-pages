---
layout: slides
title: Jekyll
---
<section markdown="block" class="intro-slide">
# {{ page.title }}

### {{ site.title }}

<p><small></small></p>
</section>

<section markdown="block">
## Ugh. Web Interface. Ugh. Build Time.

Yeah, so, GitHub pages seemed cool, __until you realized that it takes maybe a minute or so to see your changes when you use the web interface__.  Soooo..... let's abandon the whole thing!

<div class="fragment" markdown="block">
Well, __at least, don't use the web interface!__ 

# 🙅
</div>

* {:.fragment} let's develop locally (on our own computer)
* {:.fragment} and deploy to github when we're satisfied with our changes

</section>

<section markdown="block">
## Wait, Why Bother Developing Locally

__Isn't the web interface adequate?__ &rarr;

* {:.fragment} well, we just said that it's __sooooo _slow_, _rite_???__ 🐌
* {:.fragment} also, it probably makes sense to have a __development environment__ separate from your __production environment__
    * {:.fragment} so that you can test things before they go live
    * {:.fragment} so that you don't inadvertently break the site
* {:.fragment} and finally... so you can develop __with your own tools__
    * {:.fragment} you'll notice that I ❤️️ vim, and I get upset when I used a web editor
    * {:.fragment} (or it'll get filled with a bunch of h's, j's, k's, and l's - sry, vim joke, har har)

</section>

<section markdown="block">
## Local Development Overview

__To develop locally, you'll have to__ &rarr;

1. {:.fragment} create a repository on github
2. {:.fragment} either clone it or make it a remote of an existing
3. {:.fragment} write your code
4. {:.fragment} _run jekyll_ to build your site
5. {:.fragment} add, commit and push

__WAIT WAT? What's going? What's this Jekyll thing about?__
{:.fragment}


</section>

<section markdown="block">
## The Magic Behind GitHub Pages

__So... what's really happening on GitHub Pages is:__ &rarr;

1. {:.fragment} once you save a file / commit and push...
2. {:.fragment} that file is being run through a __static site generator__ (called Jekyll)
3. {:.fragment} this software goes through your files and does things like:
    * {:.fragment} __translate markdown to html__ (yeah, I bet you were wondering how that worked! no? ok nm)
    * {:.fragment} __add headers, footers and other includes__
    * {:.fragment} ...and other features (like creating blog posts!)

__This is all done automatically on GitHub's servers__ &rarr;
{:.fragment}

So... to be able to do this locally, you'll have to install Jekyll, and build your site with Jekyll
{:.fragment}
</section>



<section markdown="block">
## Demo: From Scratch with the Commandline

__Let's do a quick demo__ &rarr;

1. create a repository (you don't _have_ to configure it if you're using a GitHub pages branch)
2. git clone $SOME_REPOSITORY_URL
3. git checkout -b gh-pages
4. create an __.html__ file
5. status, add, commit
6. git push -u origin gh-pages
</section>

<section markdown="block">
## That Invovled the Follow Tools / Tech

* GitHub Pages
* git
* jekyll

__Let's go through a quick overview of each__ &rarr;

</section>

<section markdown="block">
## GitHub Pages


__So, what's GitHub Pages doing again?__ &rarr;

Basically, once you commit, it kicks off this process:

1. takes what's on your specified branch (like __gh-pages__) from your __git__ repository
2. processes it through a static site generator, __jekyll__
3. ...and hosts resulting files on github.io
4. __magic__

</section>

<section markdown="block">
## git

__What's git, what's GitHub?__ &rarr;

* {:.fragment} __git__ - the distributed version control system that we're using (why?)
* {:.fragment} __GitHub__ - a website that can serve as a remote _repository_ for your project
* {:.fragment} git != GitHub (__they're not the same thing!__)

</section>

<section markdown="block">
## git concepts

* __repository__ - the place where your version control system stores the snapshots that you _save_ (can be __local__ or __remote__)
* __branch__ - a _copy_ of your work that can be modified in parallel with other copies
* __stage__ - preparing your work to be saved
* __commit__ - saving your work
</section>

<section markdown="block">
## Some Commands

* __git clone__ - create a  _copy_ of a repository
* __git checkout -b branchname__ - create a branch
* __git status__ - what changed your repository?
* __git add__ - get ready to save your work (stage)
* __git commit__ - save
* __git push origin gh-pages__ - send your changes to a remote repository named origin
</section>


<section markdown="block">
## Jekyll

__Er - what does Jekyll exactly do?__ &rarr;

* it's a commandline __program__ (a ruby gem!)
* that __transforms/processes__ source files by...
* __copying everything in your directory into a folder called `_sites`__
* it will:
    * {:.fragment} __skip__ some things (like files that start with underscore: `_`
    * {:.fragment} __directly copy__ some files... (like `html` files, images, etc)
    * {:.fragment} and __transform__ others... 
        * like `.md` files into `.html`
        * deal with includes
{:.fragment}
</section>


<section markdown="block">
## Directory Layout

__A jekyll project comes with the following directories and files:__ &rarr;

([see the docs](https://jekyllrb.com/docs/structure/))

* {:.fragment} __`_layouts` directory__ - where you put your "surrounding" html layout
* {:.fragment} __`_includes` directory__ - where your common fragments of html live
* {:.fragment} __`_config.yml`__
* {:.fragment} __`_site` directory__ - the directory where your generated site is outputted
* {:.fragment} again, prefix with underscore means it doesn't get dropped into the \_site folder

</section>

<section markdown="block">
## Jekyll Commands

* jekyll build
* jekyll serve
* jekyll serve --watch

Or if using bundler, prefix with `bundle execd`:

* `bundel exec jekyll serve --watch`

</section>


<section markdown="block">
## Files / YAML Front Matter

_yaml front matter_ tells jekyll that it should transform the page (not just copy directly

* must be at very beginning of file
* starts and ends with three dashes
* yaml between
  * __layout__: layout file to use
  * __title__: page title

It looks something like this:

<pre><code data-trim contenteditable>---
layout: slides
title: "Static Sites and GitHub Pages"
---
</code></pre>
</section>

<section markdown="block">
## Available Variables and Tags

__"Liquid Markup"__ &rarr;

* __content__ ... where your actual file is inserted into a template
* syntax highlighting
* includes
</section>

<section markdown="block">
## So... Here's Where the Fun Begins!

(or... maybe where it gets a _little_ difficult - this could be __disastrous__!)

__Let's try bringing local Jekyll into the mix__ &rarr;

</section>

<section markdown="block">
## Requirements

__You should have this before we go on:__ &rarr;

1. [git](https://git-scm.com/book/en/v1/Getting-Started-Installing-Git) (er, I guess a gui client will work, but we'll go through commandline operations in this workshop)
2. [ruby 2.x.x](https://www.ruby-lang.org/en/documentation/installation/)
3. (maybe) bundler (you don't _really_ need to do this, but it's _best practice_ in the Ruby community)
4. `gem install jekyll` or use this guide to [install it](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/#step-2-install-jekyll-using-bundler)

<br>
Follow the instructions in [this article on installing requirements](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/#requirements): ruby, git and bundler


</section>


<section markdown="block">
## Demo: From Scratch with the Commandline

__Maybe we'll try making an adventure time fan site??? Sure. Y Not.__ &rarr;

(if this doesn't work, we can mess with the source of this site)

1. \_layouts folder
2. &#123;&#123; content &#125;&#125; tag
3. create a __.markdown__file
4. [yaml front matter](https://jekyllrb.com/docs/frontmatter/)
5. markdown!
6. [break out common elements into includes](https://jekyllrb.com/docs/includes/)
7. move items into your configuration file
8. [conditionals](http://stackoverflow.com/questions/23923416/how-do-i-create-an-if-else-statement-if-there-are-no-jekyll-posts-in-a-category)
</section>




