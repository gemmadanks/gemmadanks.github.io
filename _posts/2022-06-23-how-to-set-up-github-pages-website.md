---
title: "How to set up a GitHub pages website on a Mac"
date: 2022-06-23 T14:54:30
categories:
  - tutorials
tags:
  - setup
  - github
  - website
  - jekyll
excerpt_separator: <!--more-->
---

First things first. Getting started with open research involves choosing and setting up a way to share your work.

I have previously created several websites (my [personal website][gemma-danks], my ["astrobiology for kids" blog][pale-blue-marbles] and my [company website][octofox]). For all of these I used [WordPress][wordpress]. WordPress gives you a lot of choice when it comes to how the site looks, and is great if you don't want to edit any source code or run anything on the command line. But it can be slow, clunky and cumbersome.

[GitHub pages][github-pages] combined with [jekyll][jekyll] looks to be a better solution for documenting open research and sharing source code more easily - and it's free. It didn't take long to set up (although changing the theme was some additional work). Here's how I did it (on MacOS Monterey).

## Pre-requisites
- A GitHub account. I already had a [github account][github-gemmadanks] but if you don't then [set one up first][github] as this is required to use github pages (and an essential tool for open research if source code is involved).
- A source code editor - there are lots to choose from. I am using [VScode][vscode] for this project.
- A command line interface (I am using [iTerm2][iterm2]).

## 1. Install dependencies
1. Install [ruby][ruby], [chruby][chruby] (a package that manages ruby versions) and [jekyll][jekyll].
   
   Follow the instructions [here][chruby-instructions].

2. Install [bundler][bundler] to manage ruby gem dependencies
    ```
    gem install bundler
    ```

## 2. Set up your GitHub pages repo

Note that from this step onwards it would probably have been much quicker if I had used a template repo from the theme I eventually chose ([see below](#4-customise-jekyll-theme)).

1. **Create a new repository on GitHub**

   Follow step 1 in the [instructions][github-pages] from Github pages to [create your new repo][github-new]. 
   
   Call your new repo `username.github.io` where username is your GitHub username (mine is [`gemmadanks.github.io`][github-pages-gemmadanks]) 
   
   You will be asked if you want to add a licence for your repo. I chose an [MIT licence][mit-licence] for my source code which allows people to share it freely ([choosealicence.com][choose-a-licence] is a useful site for deciding what licence to use.)

   If you do not want your private email address to be associated with git commits, follow the instructions [here][github-private-email].
2. **Clone your new repo to your local machine** 
   
   Open a terminal, navigate to the directory you want to hold your github pages and clone your newly created repo.
   ```
   git clone https://github.com/username/username.github.io.git
   ```

## 3. Set up your jekyll site
1. Follow the instructions from GitHub [here][jekyll-site-instructions] to set up a new jekyll site.
1. Test site locally
   ```
   bundle exec jekyll serve
   ```

## 4. Customise your jekyll theme
This step can take some time! You can [choose a theme here][jekyll-theme]. I am using `minimal-mistakes` to start with as it provides all the layouts I need at the moment.

At this stage I discovered that it may have been quicker to use the [`minimal-mistakes` starter template][minimal-mistakes-starter-template] when creating the github pages repo. But the following is how I actually did it since I had already set up my repo.

1. Follow the instructions for the [remote theme method][minimal-mistakes-remote-theme] (this works well with GitHub pages).
1. I also had to add `webrick`:
   ```
   bundle add webrick
   ```
1. Copy essential template files from [starter repo][minimal-mistakes-starter-repo].

That's it! 

From here you can customise and create posts. 

## 5. Test changes
Each time you push changes to git it will regenerate the site. I recommend testing locally first. You can use the following command, copy and paste the local address into your browser and refresh the page with each change:
   ```
     bundle exec jekyll serve
   ```

Also, be sure to update `github-pages` regularly:
   ```
     bundle update github-pages
   ```

## Leave a comment below

Do you use GitHub pages? Do you have a favourite theme? Or is there an alternative platform you recommend for open research? Anything you tried that didn't work? Leave a comment below!

[bundler]: https://bundler.io/
[choose-a-licence]: https://choosealicense.com/
[chruby]: https://github.com/postmodern/chruby
[chruby-instructions]: https://jekyllrb.com/docs/installation/macos/
[gemma-danks]: https://www.gemmadanks.com
[github]: https://github.com/
[github-gemmadanks]: https://github.com/gemmadanks
[github-new]: https://github.com/new
[github-pages]: https://pages.github.com/
[github-pages-gemmadanks]: https://github.com/gemmadanks/gemmadanks.github.io
[github-private-email]: https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address
[iterm2]: https://iterm2.com/
[jekyll]: https://jekyllrb.com/
[jekyll-site-instructions]: https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll#creating-your-sites
[jekyll-theme]: http://jekyllrb.com/docs/themes/
[minimal-mistakes]: https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/
[minimal-mistakes-remote-theme]: https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/#remote-theme-method
[minimal-mistakes-starter-repo]: https://github.com/mmistakes/minimal-mistakes
[minimal-mistakes-starter-template]: https://github.com/mmistakes/mm-github-pages-starter/generate
[mit-licence]: https://github.com/gemmadanks/gemmadanks.github.io/blob/main/LICENSE
[octofox]: https://www.octofox.ai
[pale-blue-marbles]: https://www.palebluemarbles.com
[ruby]: https://www.ruby-lang.org/en/
[vscode]: https://code.visualstudio.com/
[wordpress]: https://wordpress.com/
