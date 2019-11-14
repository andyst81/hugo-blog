---
title: "Adding Elements to a Hugo a Blog"
author: "Andy T"
date: 2019-11-15
tags: ["blogging", "hugo", "disqus"]
draft: false
description: "This post details how I added Disqus comments and other elements to this blog"
featured_image: "https://images.unsplash.com/photo-1557244252-04610dfe5790?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=960&h=300"
---

I've really enjoyed playing around with Hugo over the past few weeks and am now
using it to build another site for my wife. That site is almost complete, which is
why I haven't really posted much in this site for a while. I have been playing around and adding several small things to this site though.

One very cool addition to the site has been a Disqus comment function. It was very
easy to set up as part of the Hugo framework and really worthwhile. I don't expect
a lot of comments on this blog as it is very much a collection of the information
I write as I put this website together.

Anyway, how to add Disqus to a Hugo site:

It really is as simple as signing up for a Disqus account at https://disqus.com.
Even this step is as easy as possible as you can simply register using either
Facebook, Twitter or Google. You can create the traditional way too, but I just used Twitter.

Once you've created your account, you will be asked something like "Nice! Your account has been created. What would you like to do with Disqus?  I want to comment on sites.  
I want to install Disqus on my site."

Fill in the form and create a unique Disqus name for your site - e.g. my-disqus-site-name. Remember this name -
you will then go to your config.toml file in Hugo and enter the following information

disqusShortname = "my-disqus-site-name"

You will then be able to put the following inbuilt shortcode into the code of any page
you want to have comments on:

    {{ template "_internal/disqus.html" . }}

Personally I just put the above shortcode at the bottom of my blog post template, "single.html". I think the most difficult part of this whole process was using my site name - stupidly I was using my own username for Disqus and wondering why it wasn't working!

Another small, but cool things I've added is a link to my https://dev.to profile.
dev.to is a massive inspiration for me and I really enjoy reading content on there.
If you're interested in coding and are not a member, I strongly suggest you check it out.
