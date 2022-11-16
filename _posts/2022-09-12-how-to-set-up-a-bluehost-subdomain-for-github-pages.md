---
title: "How to set up a Bluehost subdomain for a GitHub pages site"
date: 2022-09-12 T12:27:30
categories:
  - tutorials
tags:
  - setup
  - github
  - website
  - bluehost
excerpt_separator: <!--more-->  
---

I already have a [personal website][personal-website] with a page about my [previous research][previous-research], so I decided to point my open research [GitHub pages to a subdomain][github-pages-custom-domain] there rather than use the default GitHub pages url [gemmadanks.github.io][github-pages-url]. This also means it will be easier to move my site if I ever need to since I own the subdomain. 

My website is hosted at [Bluehost][bluehost]. A lot of people online recommend Bluehost and seem to like it (a lot of these people also use affiliate links for Bluehost so they make money from this recommendation). I found it to be very slow, especially for new sites, but I haven't found a better solution yet and it is cheap and fairly straightforward to manage domains there so that is what I am working with for now. 

[Adding a subdomain in the Bluehost portal][bluehost-subdomains] was easy but getting it to point to another url was not well documented so I list the steps I took below for future reference and in case others also struggle to figure it out! 

## How to set up a custom subdomain for a GitHub pages site

### Requirements
- A Bluehost account with a primary domain already set up
- A GitHub pages site already set up (read how I set mine up [here][github-pages-setup])
- 24-48 hours to wait for the subdomain to propagate
  
### 1. Create a Bluehost subdomain

1. Log in to [Bluehost][bluehost]
2. Navigate to `Domains` then `Subdomains` in the menu (to the left in my Bluehost portal page)
3. Click on the `Add subdomain` button to the top right
4. Fill in the boxes with the name of your subdomain and select your existing domain in the dropdown menu. This is how mine looked:

![Creating a subdomain on Bluehost](/assets/images/bluehost-subdomain.png)

5. Click add subdomain
6. Wait 24-48 hours for this to propagate

### 2. Point a Bluehost subdomain to your GitHub pages site

This was the poorly documented part. You will need to [add a CNAME record that points your subdomain to your GitHub pages site][github-pages-custom-domain]. How to [add a CNAME record in Bluehost][bluehost-add-cname] is well documented but what it does not mention is that first you have to remove the A records and TXT records Bluehost already added for your subdomain since it won't allow you to create a CNAME record with the same name (and you will get the error message `There was an issue adding the zone records. New Record was not inserted.`)

1. Log in to [Bluehost][bluehost]
2. Navigate to `Domains` 
3. Find your primary domain in the list and click on `Manage`. This should take you to the DNS manager. 
4. Scroll to the list of A records and find the one associated with your new subdomain (for me this was called `open-research`: you may need to click `Show all`). Remove it by clicking on the three dots to the right and selecting `remove`.
5. Scroll to the list of TXT records and find the one associated with your new subdomain (for me this was called `open-research`: you may need to click `Show all`). Remove it by clicking on the three dots to the right and selecting `remove`.
6. Scroll to the list of CNAME records. Click `Add record` and fill in the `Host record` field with your subdomain name and the `Points to` field with your GitHub Pages url. Select the minimum TTL (4 hours) from the drop down menu. Click `Save`. Mine looked like this:

![Creating a CNAME record on Bluehost](/assets/images/bluehost-cname.png)

### 3. Configure GitHub pages to use your custom subdomain
1. Navigate to your GitHub pages repo
2. Select the `Settings` tab
3. Click on `Pages` in the menu to the left under `Code and automation`
4. Scroll down to the `Custom Domain` section and add your custom domain name (mine is now `open-research.gemmadanks.com`)
5. Wait for the DNS check - if this is unsuccessful it could be that you need to wait longer for your subdomain to propagate.
6. To make your site more secure, make sure the box `Enforce HTTPS` is checked
7. Wait for the GitHub action to redeploy your site
8. Scroll back to the top of the page and check that your site now points to your custom domain (visit the site to verify)

Your GitHub pages site should now be live at your custom subdomain! Make sure you pull the changes that were made by GitHub (adding a CNAME file) to your local machine.

#### Troubleshooting
I found the following command helpful when troubleshooting. It will tell you what your subdomain is pointing to and what type of record it is using. You should see the CNAME pointing to GitHub pages listed. Open a Terminal window and paste in the following:

```
dig your-subdomain +nostats +nocomments +nocmd
```

[bluehost]: https://www.bluehost.com/
[bluehost-add-cname]: https://www.bluehost.com/hosting/help/cname
[bluehost-subdomains]: https://www.bluehost.com/help/article/subdomains
[github-pages-custom-domain]: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages
[github-pages-setup]: https://open-research.gemmadanks.com/tutorials/how-to-set-up-github-pages-website/
[github-pages-url]: https://gemmadanks.github.io
[previous-research]: https://gemmadanks.com/research
[personal-website]: https://gemmadanks.com
