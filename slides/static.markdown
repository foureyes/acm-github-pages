---
layout: slides
title: "Static Sites and GitHub Pages"
---

<section markdown="block" class="intro-slide">
# {{ page.title }}

### {{ site.title }}

<p><small></small></p>
</section>

<section markdown="block">
## So, You've Decided You Want a Website

__How 90's of you. Just make a facebook page and call it a day!__.
{:.fragment}

Nah. We're programmers, CS Majors, technofiles, [tiny cat and octopus hybrid mutants](https://octodex.github.com/), [people who like making [Byzantine complexity](https://en.wikipedia.org/wiki/Byzantine_complexity) to make their lives simultaneously easier and more _terrible_.
{:.fragment}

__So, of course, we're going to look for some options _different_ options.__ &rarr;
{:.fragment}
</section>

<section markdown="block">
## SUCH CHOICES

__What choices do we have for creating AND deploying web sites (I know, we have a lot, but... let's just talk through this)__ &rarr;

Well, we could break this up into a few broad categories...
{:.fragment}

* {:.fragment} __self hosted / cloud__ vs __self-hosted__
    * {:.fragment} __hosted / cloud__ - someone else runs the server / computing resources that you site runs own
    * {:.fragment} __self-hosted__ - you run the server that your site is hosted on
* {:.fragment} __static vs dynamic / database driven__
    * {:.fragment} __static__ - your site consists of _static_ (unchanging) files, such as plain text files (html, css, etc.) and images
    * {:.fragment} __dynamic / database driven__ - your site depends on a database, and possibly some sort of server side programming language to generate html

Of course, there are hybrids, where you may have a purely static site with no server-side language, but your site uses client site code to retrieve data from an API or database-as-a-service (Firebase, for example)
{:.fragment}

</section>

<section markdown="block">
## Static Sites Hosted on Someone Else's Platform

__For personal sites, a static site hosted on some else's servers / platform / cloud service may be a _really good_ solution. Why__ &rarr;

1. {:.fragment} __maintaining our servers is hard [let's go shopping](http://itre.cis.upenn.edu/~myl/languagelog/archives/002892.html) ([a snowclone of course](https://snowclones.org/2008/02/19/x-is-hard-let%E2%80%99s-go-shopping/))__
2. {:.fragment} seriously, __you do not want to maintain your own servers__, have to deal with security updates, make sure it's up-and-running, make sure it's not hacked into, etc. 😮 
3. {:.fragment} not everything needs a database and a server side language - writing html is just simpler ([english language and usage stackexhange, who knew?](http://english.stackexchange.com/questions/2166/more-clear-vs-clearer-when-to-use-more-instead-of-er))!
4. {:.fragment} __less points of failure__ - simply just serving static files is less prone to failure than running a database, an application server and a web server
5. {:.fragment} you're just dealing with __plain text__ (you can use text manipulation tools for finding and replacing content)

</section>



<section markdown="block">
## The World of Static Site Hosting 🌎

There are a bunch of places that'll host static sites for you __for free__ 💯 &rarr;

* {:.fragment} [Neocities](https://neocities.org/) (hey, kind of like [geocities](https://www.google.com/search?q=geocities+aesthetic&source=lnms&tbm=isch&sa=X&ved=0ahUKEwj32YWozpDSAhWqhVQKHfsFACgQ_AUICCgB&biw=1294&bih=893), but for _right now times_, instead of [1994](https://en.wikipedia.org/wiki/Yahoo!_GeoCities))
* {:.fragment} [Weebly](https://www.weebly.com/) (kind of like a _free_ squarespace maybe?)
* {:.fragment} [GitHub Pages](https://pages.github.com/) 
    * (of course, we'll be talking about this, since it's what I know)
* {:.fragment} [GitLab Pages](https://pages.gitlab.io/) (GitLab is a pretty good alternative to GitHub, and it includes a lot of similar features, like Pages - plus, you can self hoste, it has active and transparent development, etc.)
* {:.fragment} [netlify](https://www.netlify.com/home/?utm_expid=92487948-2.ORzT-7TOT0O-eMsutlXfKA.1)
* {:.fragment} [Firebase (!?)](https://firebase.google.com/docs/hosting/) (known mostly as a database-as-a-service platform, but _you can actually just serve static files from it!_)
* {:.fragment} [heroku buildpack static](https://github.com/heroku/heroku-buildpack-static) (heroku's probably not the best option for static sites, but it's possible!)
</section>


<section markdown="block">
## GitHub Pages

GitHub offers a feature called __GitHub Pages__ that __allows you to host a site directly from a GitHub repository__! &rarr;

1. {:.fragment} simply create files in your repo
2. {:.fragment} aaaaand they're _served_ (!?)
3. {:.fragment} you can reach them via `https://username.github.io/reponame` 
    * {:.fragment} (or `https://username.github.io`)
    * {:.fragment} (or you can configure a [custom domain name](), but without https)

__Some technical reasons to choose GitHub pages over some of the other solutions are__ &rarr;
{:.fragment}

* {:.fragment} you can develop with standard tools like `git`
* {:.fragment} a static site generation tool, `jekyll`, comes with it
* {:.fragment} you probably already have a project on GitHub, so hosting the accompanying site in the same place would make sense
* {:.fragment} you have https if you use the `github.io` domain 👍

</section>

<section markdown="block">
## Why Again?

__Some more _personal_ reasons to use GitHub pages__ &rarr;

* {:.fragment} it's _very_ flexible (you don't have to stick to canned templates)
* {:.fragment} you love using the commandline, so why not use that to manage your site content!? (um... _those people exist?_)

</section>

<section markdown="block">
## GitHub Pages Continued

There are some options involved with creating sites via GitHub pages. You have to determine if you want to: 

* {:.fragment} create a __user site__ (one user site per github user)  or a __project specific site__ (one site per repo)
* {:.fragment} use a pre-built jekyll theme or build from scratch
* {:.fragment} use web interface or develop locally with:
    * git
    * local jekyll
</section>

<section markdown="block">
## Using GitHub Pages

There are a few different ways to create sites using GitHub Pages.  They all require a repository on GitHub. __You can__ &rarr;

* use the web interface
* use the commandline
    * plain html
    * with layouts, markdown
</section>

<section markdown="block">
## "Simple" Set Up

__To set up a static site with GitHub pages using a pre-built theme__ &rarr;

1. {:.fragment} __create a repository__
    1. {:.fragment} initialize with jekyll in your `.gitignore` (this will keep unwanted files out of your repository)
    2. {:.fragment} optionally add a `README.md` file
2. {:.fragment} if this site is meant to accompany code for a project that's in the same repository, __create a new branch__ (a good convention is to use `gh-pages` as the branch name)
3. {:.fragment} __configure your repository__ to use GitHub pages
    1. {:.fragment} __specify the branch__ (stick with `master` or use the branch you created above, like `gh-pages`)
    2. {:.fragment} choose a theme

[Check out the GitHub pages guide for a full guide](https://pages.github.com/)
{:.fragment}

</section>

<section markdown="block">
## Adding Pages to Your Static Site

__To add some html files to your site__ &rarr;

1. {:.fragment} change to the branch that you configured for use with GitHub Pages
2. {:.fragment} create a new file with an html extension (remember to add the file name!)
    1. {:.fragment} add this header to the file:
        <pre><code data-trim contenteditable>
---
layout: default
---
    2. {:.fragment} add your markup:
        <pre><code data-trim contenteditable>
        <h1>Sooo static</h1>
</code></pre>
3. {:.fragment} add your comment and commit
4. {:.fragment} check out your page:
    * go to https://username.github.io/reponame
    * or just https://user.github.io for a user site

__You'll have to wait for about 30 seconds or so to see your page build__ 😢
{:.fragment}
</section>

<section markdown="block">
## My Eyes are Bleeding Angle Brackets

__You know what makes me cry? HTML. So many pointy angle brackets, so many tags!__ 😭

Don't worry! GitHub pages allows you to write up some markdown instead of html! __Let's try it__ &rarr;
{:.fragment}

1. {:.fragment} start with the header - `layout: default`
2. {:.fragment} __give your file an `.md` extension__
3. {:.fragment} write u sum markdown!
4. {:.fragment} (uh, what's markdown?)


</section>

<section markdown="block">
## Markdown 

__Markdown is a lightweight markup language meant to mimic the format of text files and yet, be easily converted to html__ &rarr;

There's the canonical [markdown syntax from daring fireball](https://daringfireball.net/projects/markdown/syntax), but we'll be using [github flavored markdown](https://guides.github.com/features/mastering-markdown/) and _jekyll_. This allows for:
{:.fragment}

* {:.fragment} mixing html with markdown
* {:.fragment} code blocks
* {:.fragment} tables

</section>

<section markdown="block">
## GitHub Markdown

__Again, check out the [reference](https://guides.github.com/features/mastering-markdown/). Let's go over...__

* {:.fragment} headers
* {:.fragment} lists
* {:.fragment} block quotes
* {:.fragment} links
* {:.fragment} images
* {:.fragment} inline code
* {:.fragment} code blocks with fences and indentation
* {:.fragment} mixing in markup

</section>


