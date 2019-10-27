---
title: "Blog Building"
author: "Andy T"
date: 2019-10-27
tags: ["blogging", "hugo", "skeleton", "bootstrap"]
draft: false
description: "An update detailing what I've done with this blog so far"
featured_image: "https://images.unsplash.com/photo-1519337265831-281ec6cc8514?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=967&h=300"
---

I've been working on this blog for some time now and I think it's worthwhile
to document what I've done so far, just in case it's helpful for other people.
I mentioned in a previous post that I'm building this site with Hugo static site
generator. Initially I followed a tutorial from Zachary Wade Betz, on how to
build a Hugo blog from scratch. The tutorial can be found here [Hugo Tutorial](https://zwbetz.com/make-a-hugo-blog-from-scratch/) and truly is
a great way to get accustomed to the structure of Hugo and how to use it to build
a great website.

If you follow along with the tutorial, you will see the similarities in styling between this site and the one created in the tutorial. Since completing the tutorial, I have
made a few modifications to the site to make it more inline with what I like.
The first modification I made was to move from Bootstrap to Skeleton. I've always
found Bootstrap to be quite unwieldy due to the sheer number of options it has.
As such, I was on the lookout for a similar, but much easier to handle framework
and I believe I have found that - [Skeleton](http://getskeleton.com/).

Skeleton is a very lightweight boilerplate for simple web design. It is only
around 400 lines of CSS, focused on the most common HTML elements. It's certainly
not suitable for every project, but for a simple blog with minimal styling, it's
perfect. The best part is that it's not a million miles away from Bootstrap, so
the conversion was fairly painless. I had to reclassify a few elements, but the
whole process of migrating to Skeleton from Bootstrap probably look less than an
hour.

To make the migration, I simply downloaded the [Skeleton CSS file](https://raw.githubusercontent.com/dhg/Skeleton/master/css/skeleton.css), as well as the
[Normalize CSS](https://raw.githubusercontent.com/dhg/Skeleton/master/css/normalize.css)
files and copied them into the 'static/css' directory of my blog project. I made sure to
search for Bootstrap across the whole project and made sure to link to
Skeleton instead. Then I created a 'stylesheet.css' file to manually add any other
stylings required.   

After migrating to Skeleton, the next thing I wanted to do was migrate the icons to
FontAwesome. I'm a pro FontAwesome subscriber after contributing to their
KickStarter campaign for FA5 several years ago. FontAwesome have a lot more icons
to choose from and I think their icons just look a bit better too, so the switch
was a good move for me. Again this didn't take a huge amount of time. I had to
create a kit inside FontAwesome and put the link to that kit in my 'head.html' partial.
Then I had to rename the "Pre" section for each menu item in 'config.toml' to the FontAwesome name. I also went through and changed the other icons in the blog,
such as the 'tags'.

On the subject of fonts, I also changed the typography of the site by adding a
couple of Google Fonts to the site. This was simply a matter of finding the fonts
that I like and copying the convenient code Google Fonts provides into my
'stylesheet.css' file and editing the relevant elements.

The most difficult thing I did was creating a responsive mobile 'hamburger' menu.
I looked through quite a lot of responsive Hugo themes and tried to copy from them,
but I kept running into problems - either with the styling, or messing up the menu
on desktop or even just disappearing completely. In the end I was able to modify
[this tutorial](https://www.w3schools.com/howto/howto_js_topnav_responsive.asp)
from W3. On Skeleton, the code in this tutorial worked well, after a little tweaking
of classes.

I used the 'Audit' function in Google Chrome to analyse the site's performance and
there were a lot of minor tweaks required to improve the scores there, but that's
a post for another time.

I still have several other things that I want to implement on this blog. Next up
I will add a function to add comments, and I will also add pagination once I have more
than 10 posts. I'd also like to implement a 'robots.txt' file, even though I realise it's not really that necessary for a site like this - I just want to do more things.I'm sure that I'm not done with the styling yet either.

Thanks for reading!
