---
layout: slides
title: "Hi!"
---
<section markdown="block" class="intro-slide">
# {{ page.title }}

### {{ site.title }}

<p><small></small></p>
</section>

<section markdown="block">
## New Phone, Who Dis?

It's me, __Joe Versoza__! &rarr;

* {:.fragment} I'm a __Clinical Assistant Professor__ here at NYU's CS Department
* {:.fragment} Maybe you know me already?
    * {:.fragment} I teach a class on __Applied Internet Technology__ (read: fancy words for node and Express)
    * {:.fragment} ...and a bunch of intro courses (__Intro to Programming__, CS, etc.)
    * {:.fragment} Some people think I give _a lot_ of homework  (I think I don't, ¯\\_(ツ)_/¯ ) 
    * {:.fragment} Don't worry, there's __no homework 4 U.__

I'm giving this talk because some of your fellow students / ACM members _thought_ I knew stuff about it (I do _sort of_ ... but mainly because __all of my course sites are built with the technologies we'll discuss__)
{:.fragment} 
   

</section>

<section markdown="block">
## And You?

__A little about you! ...Perhaps__ &rarr;

* {:.fragment} you want to build a __personal web site__ / a site for your project
* {:.fragment} you're interested in doing this using GitHub's "Pages" __for free__
* {:.fragment} you're comfortable using $YOUR_FAVORITE_TEXT_EDITOR
* {:.fragment} you're ok with mashing your keyboard to produce some commandline incantations
    * {:.fragment} you can maybe get around on the commandline (`cd` mostly)
    * {:.fragment} you don't have to know too much git, but it would be nice if you have _some_ familiarity with it

</section>


<section markdown="block">
## BTW...

__How many people have experience with__ &rarr;

(raise both hands 🙌 if you _actually_ use it every now and then vs one hand ✋ for "I used it once in a fever dream")
{:.fragment}

* {:.fragment} git 
* {:.fragment} GitHub 
* {:.fragment} commandline?
* {:.fragment} gems?
* {:.fragment} markdown?
* {:.fragment} jekyll?

</section>

<section markdown="block">
# If you already have used GitHub pages and Jekyll, you'll probably be bored

(maybe buy some Valentine's day candies and watch a romantic comedy instead of staying here? 💖💖💖)

</section>
<section markdown="block">
## About This Workshop

__So, what _exactly_ are we all doing here?__ &rarr;

* {:.fragment} we'll be looking at a few ways of creating static websites using...
    * {:.fragment} __GitHub Pages__
    * {:.fragment} __Jekyll__
    * {:.fragment} __markdown__
    * {:.fragment} __git__
* {:.fragment} we'll do this starting with the easiest way... and incrementally use more and more powerful tools / methods
    1. {:.fragment} first, just through GitHub's web interface with a pre-built theme
    2. {:.fragment} ...all the way through building a site locally and using pushing to GitHub for _publication_

</section>
<section markdown="block">
## Required Software

__You'll need this to get through the more _intermediate_ level stuff:__ &rarr;

1. [git](https://git-scm.com/book/en/v1/Getting-Started-Installing-Git)
2. [ruby 2.x.x](https://www.ruby-lang.org/en/documentation/installation/)
3. (maybe) bundler <-- things can work fine without this

<br>
Check out [this article on installing requirements](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/#requirements)
</section>


<section markdown="block">
## These Slides

Hey - have you ever heard of the term __eating your own dogfood__ / _dogfooding_ in the context of technology or business? __Sounds gross. What is it?__ &rarr;

Via [wikipedia](https://en.wikipedia.org/wiki/Eating_your_own_dog_food) (yes, it has its own wikipedia page):
{:.fragment}

>  a scenario in which a company uses its own product to test and promote the product
{:.fragment}

* {:.fragment} So... of course, if I'm giving a talk about GitHub Pages and Jekyll, this site was __built with GitHub Pages!__
* {:.fragment} (and additionally, some other things outside of the scope of this talk, like [reveal.js](http://lab.hakim.se/reveal-js/#/) for slides, [grunt](http://gruntjs.com/) for "task automation", and a tiny bit of [bootstrap](http://getbootstrap.com/))
* {:.fragment} _fun fact_ (if this is your idea of fun), but I think that the bootstrap site is also [hosted on GitHub Pages](https://github.com/twbs/bootstrap/tree/gh-pages)
* {:.fragment} you can also click on the __print__ link to get the one-page version of the slides
</section>

<section markdown="block">
## Some Examples of Sites on GitHub Pages

__Before we go on. (yup, they're all hosted on GitHub Pages)__ &rarr;

* [javascript games](http://basicallydan.github.io/skifree.js/)
* As we said:
    * [Twitter's Bootstrap project page](http://twitter.github.io/bootstrap/)
    * and of course, [this presentation](http://foureyes.github.io/acm-github-pages/)
* [Facebook's React](https://facebook.github.io/react/) Check. That. URL. 😎
* [Microsoft's Open Source Projects](https://opensource.microsoft.com/)
* [...and many others](https://github.com/showcases/github-pages-examples)
</section>

