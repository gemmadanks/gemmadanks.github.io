---
title: "How to use jekyll-scholar with GitHub Pages"
date: 2022-11-23 T12:54:30
categories:
  - tutorials
tags:
  - setup
  - github
  - website
  - jekyll
  - tools
excerpt_separator: <!--more-->
---
[Jekyll-scholar][jekyll-scholar] is a plugin that generates bibliographies and in-text citations, formatted according to any one of hundreds of citation styles. Getting it to work with [GitHub Pages][github-pages] was not so easy.

## Why jekyll-scholar?
I am at the literature review stage of [my research process][my-research-process] and, as I want to document each step, I thought I'd write a few posts on the papers and background topics I was reading. I soon realised, however, that I didn't know how to add citations and generate a reference list in my markdown files ([LaTex][latex] and [BibTex][bibtex] have been my tools of choice for academic writing until now) in a way that works with [jekyll][jekyll] and [GitHub Pages][github-pages] and avoids me adding them manually (which does not scale).

Some googling led me to the [jekyll-scholar][jekyll-scholar] plugin, which seems popular and sounded like exactly what I need. As usual with these things though, I quickly ran into some issues that took several hours to resolve. 

In case it's helpful to others, here's what I had to do to get jekyll-scholar to work on my GitHub Pages site. 

## How to use jekyll-scholar with github-pages

### 1. Use GitHub Actions to build and deploy GitHub Pages site
For security reasons, only a limited number of [third-party plugins are supported by the GitHub Pages][github-pages-dependencies] automated build pipeline using the default ```'Deploy from a branch'``` method. It is possible, however, to use GitHub's continuous integration and continuous delivery (CI/CD) platform, [Github Actions][github-actions], and [create a custom workflow][github-actions-github-pages] that installs any jekyll plugin. This is actually very easy to do from your GitHub Pages repository page:  

1. Open the ```Settings```--> ```Pages``` tab 
2. Under ```'Build and Deployment'```, change the ```'Source'``` from ```'Deploy from a branch'``` to ```'GitHub Actions'```
3. Add the suggested workflow yaml file (saved under ```.github/workflows```)

You can see my final workflow file [here][github-workflow].

Note: if you have a ```Gemfile.lock``` file committed to your repo then it may cause issues: add it to ```.gitignore```and remove it from your git cache (```git rm --cache Gemfile.lock```)

### 2. Add the jekyll-scholar plugin
This is also straightforward:
1. Add ```gem "jekyll-scholar", group: :jekyll_plugins``` to your ```Gemfile``` (you can see mine [here][gemfile])
2. Add ```- jekyll-scholar``` to your ```_config.yml``` (see mine [here][config])

### 3. Downgrade ruby
Ideally, the two steps above would be all that is needed to get up and running with jekyll-scholar on GitHub Pages but when I tried adding a citation and building my site locally I got the error message ```Liquid Exception: tried to create Proc object without a block```. 

After a lot of googling I landed on the most likely source of the problem being [incompatible ruby versions][ruby-issue] between [github-pages][github-pages-gems] and jekyll-scholar. I have not spent a lot of time trying to dig into this to figure out why it is an issue, or if there is a better way to solve it, but downgrading ruby from ```3.1.2``` to ```2.7.2``` solved the problem and so this is what I am doing for now.

#### Downgrade ruby locally
1. Install older ruby version locally using [chruby][chruby] (```ruby-install 2.7.2```)
2. Restart your terminal
3. Select older ruby version with ```chruby 2.7.2```
4. Re-run ```bundle install``` to update gems
5. Run ```bundle exec jekyll serve``` to validate fix

#### Downgrade ruby in build pipeline
1. Add a ```.ruby-version``` file to the root of your repo and specify ruby version ```2.7.2```
2. Remove the ruby version line from the ```jekyll.yml``` workflow

### 4. Add a BibTex file with a list of references
Export a list of references in BibTex format from your reference manager, name it ```references.bib``` and place this file into a new folder called ```_bibliography```.

### 5. Choose a citation style
The default style used by jekyll-scholar is [apa][apa-csl] but this can be changed in the ```_config.yml``` file to any [csl style][csl-styles] (I found the [style repository][zotero-style-repo] from [Zotero][zotero] useful for choosing one of these).

#### How to remove the duplicate numbers using a numeric citation style with jekyll-scholar
I wanted a numeric citation style and ran into difficulty with the list of references doubling up on the numbers (see the issues reported [here][jekyll-scholar-issue-75] and [here][jekyll-scholar-issue-160]). This is due to jekyll-scholar using an ordered list for the references, which by default adds extra numbers. 

I used the solution suggested by the developer and added ```<style>ol.bibliography li { list-style: none }</style>``` to the layout file of my posts. This results in a [list without numbers][html-list-style] but it does not offset the numbers as it should according to the style. I will look into this further at a later date.

### 6. Add citations and a reference list
You can now add citations and lists of references following the syntax described [here][jekyll-scholar-citations]. 

For example, here is a reference to one of the first SETI papers {% cite Cocconi1959 %}. 

Now I can get on with my literature review and make notes with citations as I go along.

#### References

{% bibliography --cited %}

[apa-csl]: https://github.com/citation-style-language/styles/blob/master/apa.csl 
[bibtex]: http://www.bibtex.org/
[chruby]: https://github.com/postmodern/chruby
[config]: https://github.com/gemmadanks/gemmadanks.github.io/blob/main/_config.yml
[csl-styles]: https://github.com/citation-style-language/styles
[gemfile]: https://github.com/gemmadanks/gemmadanks.github.io/blob/main/Gemfile
[github-actions]: https://docs.github.com/en/actions
[github-actions-github-pages]: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow
[github-pages]: https://pages.github.com/
[github-pages-dependencies]: https://pages.github.com/versions
[github-pages-gems]: https://rubygems.org/gems/github-pages/versions/227
[github-workflow]: https://github.com/gemmadanks/gemmadanks.github.io/blob/main/.github/workflows/jekyll.yml
[html-list-style]: https://developer.mozilla.org/en-US/docs/Web/CSS/list-style
[jekyll]: https://jekyllrb.com/
[jekyll-scholar]: https://github.com/inukshuk/jekyll-scholar
[jekyll-scholar-citations]: https://github.com/inukshuk/jekyll-scholar#citations
[jekyll-scholar-issue-75]: https://github.com/inukshuk/jekyll-scholar/issues/75
[jekyll-scholar-issue-160]: https://github.com/inukshuk/jekyll-scholar/issues/160
[latex]: https://www.latex-project.org/
[my-research-process]: https://open-research.gemmadanks.com/planning/my-research-process/
[ruby-issue]: https://github.com/alshedivat/al-folio/issues/161
[zotero]: https://www.zotero.org/
[zotero-style-repo]: https://www.zotero.org/styles