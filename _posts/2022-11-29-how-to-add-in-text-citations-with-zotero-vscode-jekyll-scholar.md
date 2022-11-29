---
title: "How to add in-text citations in jekyll-scholar format in VS Code using Zotero"
date: 2022-11-29 T11:00:00
categories:
  - tutorials
tags:
  - setup
  - github
  - website
  - jekyll-scholar
  - tools
  - zotero
  - citations
---

This post documents how to "cite while you write" in [VS Code][vscode] using the reference manager [Zotero][zotero] and the [Better BibTex extension][better-bibtex] when you are using the static site generator, [Jekyll][jekyll], and the [jekyll-scholar][jekyll-scholar] plugin for handling citations. This makes academic writing on a [GitHub Pages][github-pages] site much easier.

Making all of my work open involves some technical challenges to overcome so I am also documenting these in case it helps others. 

Previous posts include:

1. [How to set up a GitHub pages website on a Mac][github-pages-how-to] 
2. [How to set up a Bluehost subdomain for a GitHub pages site][custom-domain-bluehost-how-to]
3. [How to use jekyll-scholar with GitHub Pages][jekyll-scholar-how-to]

## Jekyll-scholar and VS Code
I use [VS Code][vscode] for writing both code and [my posts][posts]. The latter are all written in [markdown][markdown] (you can see the [raw files here][posts-md]). 

In order to add citations to my posts I decided to use [jekyll-scholar][jekyll-scholar]. This requires references in BibTex format (most reference managers will export these - you can [see mine here][references-bibtex]). You can then add in-text citations to a markdown post using the following code snippet:

```{% raw %}{% cite CitationKey %}{% endraw %}```

Where ```CitationKey``` matches the key in your BibTex references file for the reference you want to cite. 

The following snippet at the end of the post renders a list of references:

```{% raw %}{% bibliography --cited %}{% endraw %}```

There are lots of ways to [customise both in-text citations and the bibliography with jekyll-scholar][jekyll-scholar-citations]. It is cumbersome, however, to go to your BibTex file (or your referencee manager), find the paper you want to cite, copy the citation key then type it into the format above. [Using a generated code snippet][vscode-code-snippet] would speed up the process but not enough. I wanted it to be more streamlined. 

## Zotero and Better BibTex
After some googling, I decided to try the reference manager, [Zotero][zotero], together with the [Better BibTex extension][better-bibtex]. These allow a lot of customisation and integration with other tools, including VS Code. Zotero also has a plugin for web browsers that allows you to import papers into different collections. It is also free and open-source.

Importantly, Zotero allows in-text citations to be added using drag and drop from the desktop app and there is a third-party VS Code plugin, ['Citation Picker for Zotero'][zotero-citation-picker], that allows you to search your library and insert citations from within VS Code itself. 

This Zotero-based setup sounded like exactly what I needed but it required some tweaking of the settings to get it to insert citations in the right format for [jekyll-scholar][jekyll-scholar-citations].

## How to 'cite while you write' in VS Code with Zotero and jekyll-scholar
There are two main ways (not including manually typing in the citations) to add in-text citations while you write:
1. Drag and drop from [Zotero][zotero] using [Better BibTex][better-bibtex]
2. ['Citation Picker for Zotero'][zotero-citation-picker] within [VS Code][vscode]

By defaut either way inserts in the pandoc format ```@CitationKey```. This is great if you are using pandoc to convert markdown to pdf but it doesn't work with jekyll-scholar. Here's how to get the citations into jekyll-scholar format.

### Requirements
- [VS Code][vscode] and the ['Citation Picker for Zotero'][zotero-citation-picker] plugin
- [Zotero][zotero]
- [Better BibTex][better-bibtex]
- A [Jekyll][jekyll] site (e.g. [GitHub Pages][github-pages]: [here's how I set mine up][github-pages-how-to])
- [jekyll-scholar][jekyll-scholar] ([here's how I got jekyll-scholar to work with GitHub Pages][jekyll-scholar-how-to])
  
### How to get 'Citation Picker for Zotero' to insert citations in jekyll-scholar format
Luckily [Better BibTex has a way to customise the format for in-text citations][better-bibtex-cite-diy] and this can be accessed by changing the URL in the settings of the ['Citation Picker for Zotero'][zotero-citation-picker] plugin.

There are several ready-made formatters but none for [jekyll-scholar][jekyll-scholar] so I used the ```playground``` formatter with custom ```citeprefix```, ```citepostfix``` and ```separator``` to create a string that generates citations in the correct format.

1. In VS Code, navigate to the settings of the ['Citation Picker for Zotero'][zotero-citation-picker] plugin
2. Replace the URL for the port picker with the following:

```http://127.0.0.1:23119/better-bibtex/cayw?format=playground&citeprefix=%7B%25%20cite%20&citepostfix=%20%25%7D&separator=%20``` 

The ```citeprefix``` is the part of the citaton string before the citation key (```{% raw %}{% cite {% endraw %}``` using [hexadecimal][hexadecimal-converter] for special characters) and the ```citepostfix``` is the part of the citation string after the citation key (```{% raw %} %}{% endraw %}```). The ```separator``` parameter puts spaces between multiple citation keys (the default is ```,```).

{:start="3"}
3. Restart VS Code and make sure you have Zotero running
4. Open a markdown file and find a place you want to add a citation
5. Open the Command Palette (```Ctrl-Shift-P``` on a Mac) and select ```Zotero Citation Picker```
6. Wait for the citation picker to open
7. Search for your citation and add it
8. When you run jekyll serve it will render the citation in the style you have chosen for jekyll-scholar 


### How to get Zotero to insert citations in jekyll-scholar format using drag and drop and Better BibTex
I also wanted to be able to drag and drop citations from the Zotero desktop app. To do this I had to edit the ```Quick-Copy``` settings in Zotero and create a [custom Eta template][better-bibtex-eta].

1. In Zotero navigate to ```Preferences --> Better BibTex --> Export --> Quick-Copy```
2. Under ```Quick-Copy format``` select ```Eta template```
3. Paste the following into the box:

```{% raw %}{% cite <% for (const item of it.items) {%> <%= item.citationKey %> <% } %> %}{% endraw %}```
 
 This outputs the prefix string, iterates through and outputs the citation keys with spaces in between and then adds the postfix string.

## Share your thoughts
What tools do you use for managing citations? Do you have any tips or tricks for academic writing on open platforms? Was this post helpful? Let me know in the comments! 


[better-bibtex]: https://retorque.re/zotero-better-bibtex/
[better-bibtex-cite-diy]: https://retorque.re/zotero-better-bibtex/citing/cayw/#diy
[better-bibtex-eta]: https://retorque.re/zotero-better-bibtex/installation/preferences/export/#eta-template
[custom-domain-bluehost-how-to]: https://open-research.gemmadanks.com/tutorials/how-to-set-up-a-bluehost-subdomain-for-github-pages/
[github-pages]: https://pages.github.com/
[github-pages-how-to]: https://open-research.gemmadanks.com/tutorials/how-to-set-up-github-pages-website/
[hexadecimal-converter]: https://www.rapidtables.com/convert/number/ascii-to-hex.html
[jekyll]: https://jekyllrb.com/
[jekyll-scholar]: https://github.com/inukshuk/jekyll-scholar
[jekyll-scholar-how-to]: https://open-research.gemmadanks.com/tutorials/how-to-use-jekyll-scholar-with-github-pages/
[jekyll-scholar-citations]: https://github.com/inukshuk/jekyll-scholar#citations
[markdown]: https://www.markdownguide.org/
[mendeley]: https://www.mendeley.com/search/
[posts]: https://open-research.gemmadanks.com/posts/
[posts-md]: https://github.com/gemmadanks/gemmadanks.github.io/tree/main/_posts
[references-bibtex]: https://github.com/gemmadanks/gemmadanks.github.io/blob/main/_bibliography/references.bib
[vscode]: https://code.visualstudio.com/
[vscode-code-snippet]: https://code.visualstudio.com/docs/editor/userdefinedsnippets
[zotero]: https://www.zotero.org/
[zotero-citation-picker]: https://marketplace.visualstudio.com/items?itemName=mblode.zotero&ssr=false#overview