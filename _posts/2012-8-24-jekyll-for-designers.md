---
layout: post
title: Jekyll for Designers
image: 
---

For the first post on my new site I figured it would only be appropriate if I wrote about how I went about creating the site in the first place. It was a bit of a journey experimenting with different platforms, but I ultimately ended up with [Jekyll](https://github.com/mojombo/jekyll) and I'm glad I did. Let me tell you why.

## Cheap Bastard
My roommate, [Jeremy Franz](http://jeremyfranz.com/), initially turned me on to [Jekyll Bootstrap](http://jekyllbootstrap.com/) and [Octopress](http://octopress.org/) as some good options for a blogging platform that are easy to set up and deploy at no cost through GitHub Pages or Heroku. I set up both, but quickly found that the assumptions and out of the box styling of the frameworks end up causing more trouble than they're worth for what I was trying to do. If you need a blog in a snap, that's the way to go, but I knew I wanted to write mine from scratch.

I wanted something simpler, so I dug deeper into using just Jekyll. Jekyll is described as 
>"a simple, blog aware, static site generator. It takes a template directory (representing the raw form of a website), runs it through Textile or Markdown and Liquid converters, and spits out a complete, static website suitable for serving with Apache or your favorite web server."

Markdown, so hot right now. Sounds like what I'm looking for.

Jekyll just makes sense for designers. It uses the [Liquid Templating Language](http://liquidmarkup.org/) which is about as simple and human readable as it gets. There's also a nice little [wiki](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers) made just for us dumb designers. Throw in a few lines of liquid and your static site will be faking dynamic content in no time!

## Have Mercy
If GitHub feels foreign to you, not to worry. We're just going to have to take a few steps back before we start. There are some prerequisites like XCode, Git, Ruby Version Manager (RVM), and Ruby that are necessary just to get your development environment up to speed. Here's [a comprehensive guide](http://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/) that covers a few different versions of OSX. If this is all new to you, don't be afraid of the command line. It will be uncomfortable at first, but that will pass. Comfortable is what we're aiming for, not expertise.

## Jekyll for Designers
Now, for the scary part. Setting up Jekyll and the designer dreaded command line. Don't worry, it will only hurt for a second. A great place to start, as with anything, is with the original [Jekyll Documentation](https://github.com/mojombo/jekyll/wiki).

I created a public repo on GitHub named after this post called [Jekyll For Designers](https://github.com/Mukealicious/Jekyll-for-Designers). It has the basic base code and instructions for getting Jekyll up and running and deploying to Heroku, easy as pie. Also, all of the code for this very site using Jekyll is available on [my Muke.me repo](https://github.com/Mukealicious/mukealicious.github.com) for reference. If you run into a dead end, see how I did it. After all, that's how I made it through my initial setup.

### Initial Configuration
After forking the [Jekyll For Designers](https://github.com/Mukealicious/Jekyll-for-Designers) repo head to the local project direcotry on your machine in terminal and run

```bundle install```

Now you have all of the necessary gems installed that were listed in the Gemfile you forked. To compile your site and see a preview run

```jekyll --server```

Head over to http://localhost:4000/ to see "Hello World"

Your Jekyll install is up and running and ready to deploy! You will need to have git and heroku command line tools installed in order to deploy. These are available in the [Heroku Toolbelt](https://toolbelt.heroku.com/) if you don't have them already. 

```heroku create -s cedar --buildpack http://github.com/mattmanning/heroku-buildpack-ruby-jekyll.git```

Push to heroku

```git push heroku master```

That's it!

### Jekyll to GitHub Pages
If you want to deploy your Jekyll site through GitHub Pages instead of Heroku, then there are plenty of good resources out there for that. After all, that is what Jekyll was created to do. [Jekyll Base](https://github.com/danielmcgraw/Jekyll-Base) by Daniel McGraw should do the trick.

## Now, That Wasn't So Bad Was It?
The command line can be scary, but with some experimentation and a little courage you'll be deploying like a boss in no time. If you want to make Jekyll real fancy and write posts in the browser, check out [Prose](http://prose.io/). It's like a CMS style backend for GitHub repos.

### Further Reading
There's plenty more to be learned to master Jekyll, Liquid, and Markdown. Here's some further reading and resources I've found useful in my random walk.

#### Jekyll
- [Jekyll Bootstrap's Intro To Jekyll](http://jekyllbootstrap.com/lessons/jekyll-introduction.html)

#### Liquid
- [Shopify's Liquid for Designers](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers)

#### Markdown
- [Daring Fireball Markdown Syntax](http://daringfireball.net/projects/markdown/syntax)
- [Mou App](http://mouapp.com/)
- [iA Writer](http://www.iawriter.com/)