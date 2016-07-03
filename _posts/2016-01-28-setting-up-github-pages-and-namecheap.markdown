---
layout: "post"
title: "Part Two: Setting Up GitHub Pages and Namecheap"
date: "2016-01-28 19:02"
categories: githubpages namecheap web
tags: githubpages namecheap web
image: /images/Banner.png
---

>This post is going to assume that you have already set up a Namecheap account using your GitHub Student Developer pack and picked out a fancy domain name for yourself. So even though this post is labeled as "Part Two”, please realize that I did not provide a "Part 1" because I thought that part one (“Setting up your Namecheap Account”) was straight forward enough to skip.

After you created your free .me domain from Namecheap and you opted in for free GitHub Pages hosting, then your Github account should have a new repository. This repository should look pretty bland with only a `README.md` file visible. But you should notice that there are two branches: `master` and `gh-pages`.

<img src="/images/postimg/4.png" class="image postimg image left" alt="Github Branches" />

The gh-pages branch will contain anything pertaining to your website. Navigate to the gh-pages branch and add a new file. Name the file `CNAME` and type in the domain name you received from Namecheap (for me this was “catslove.me”).

Commit the changes and navigate back to the gh-pages branch and click on “Settings”. Scroll down to the “GitHub Pages” section and you should see a green checkmark next to, “Your site is published at http://(insert domain name here).”

<img src="/images/postimg/gitpagescheck.png" class="image postimg" alt="GitHub Pages Checkmark" />

If you don’t see this then go to the troubleshooting section below. Now let’s go ahead and create your first HTML page. In the gh-pages branch add a new file, we will name it index.html, and add the following text:

```
<!DOCTYPE html>
<html>
  <head>
    <title>Hi! This is my first page!</title>
  </head>
  <body>
    <h2>I love cats!</h2>
  </body>
</html>
```
Commit changes and go visit your domain. Congratulations! You should now see some text on your webpage.

----------

Using GitHub’s Automatic Page Generator:
-------------
<img src="/images/postimg/githubsitebuilder.png" class="image postimg" alt="GitHub Pages Site Generator Example" />
Whether or not you enjoy deckin’ out webpages, I suggest that you try out GitHub’s automatic page generator just for fun and experience. To use GitHub’s automatic page generator just go to your repository, click on “Settings”, and scroll back down to the “GitHub Pages” area. Click “Launch automatic page generator” and walk through the steps. In the generator you can give your page a name and select a layout. When you complete the process go check it out on your now spiffy domain. If you decide you don’t like the site, then you can always roll back changes or delete everything except the `CMAKE` file in the gh-pages branch.

What Now?
-------------
If you are satisfied with GitHub pages as it is, then you can go ahead and create your own website. GitHub pages should work with any non-server side languages. If you are interested in having a blog, and not just a static website for free though, then you have a few options. One option is to continue using GitHub as your site host and set up Jekyll to work with GitHub pages. The other option is to pick one of the cloud computing platforms that was included in the Student Developer Pack (such as Digital Ocean or Amazon Web Services), launch a server, install and configure a blogging platform such as Wordpress, and hook up your domain to your server. Both of these options will be covered on this blog and both options have their own pros and cons.

Troubleshooting:
-------------
If you selected the GitHub pages option when you received your domain name then Namecheap should have set everything up for you on their side. Otherwise you might have to manually set up this step. Go to Namecheap.com and sign in to your account. You should be taken to your Namecheap dashboard. Click on Domain List and you should see a list of your domains. Click on the manage button next to the domain you just created and go to the "Advance DNS" tab. Make sure you have the following listed:

```
A Record      @     192.30.252.153  30 mins
A Record      @     192.30.252.154  30 mins
CNAME Record  www   catslove.me     30 mins
```
If you don't have the first two listed go ahead and add them now, as they are required to link up to GitHub Page's hosting. Not having records listed is one of the most common issues when it comes to your website not being hooked up correctly. When you add these records make sure you give the DNS 24 hours to sync.

If you already have these records added and you still can't get your website hosted correctly you should go ahead and contact Namecheap support.
