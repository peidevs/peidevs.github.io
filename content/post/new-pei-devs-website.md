+++
categories = []
date = "2017-05-10T22:36:55Z"
description = ""
draft = true
tags = []
thumbnail = ""
title = "New PEI Devs Website"

+++
In July 2015 the group determined we should have some web presence to create a compilation of all of our resources in one area. [Michael](https://twitter.com/codetojoy) stepped up and created us a very simple bootstrap website with all of the resources jammed on the site to have the single source of information we desired.

We knew this was never going to have this as a long term solution and started thinking about what we wanted for a website. September of 2015 an [issue](https://github.com/peidevs/peidevs.github.io/issues/2) was logged to start revamping to have a proper website. <span style="font-size: 1rem;">Around this time we met the folks at </span><a href="https://forestry.io/" style="font-size: 1rem; background-color: rgb(255, 255, 255);">Forestry.io</a><span style="font-size: 1rem;"> who introduced us to static website generators </span><a href="https://jekyllrb.com/" style="font-size: 1rem; background-color: rgb(255, 255, 255);">Jekyll</a><span style="font-size: 1rem;"> and </span><a href="https://gohugo.io/" style="font-size: 1rem; background-color: rgb(255, 255, 255);">Hugo</a>

The rest of this document will talk about the technical hurdles and lessons learned from this project.

### Stage 1 - Deep Dive into Jekyll with our own theme

The initial work on the new site started in June 2016. I have never used a static site generator before so I just picked one to try. I dove head first into Jekyll because it was the first one mentioned to me. At the time I was playing around with Flexbox quite a bit so I decided to roll my own theme during this process (wrong choice).

Jekyll runs off Ruby, so the first battle with using Jekyll was getting Ruby installed on my macbook. like most, first thing I run is `ruby --version`<span style="font-size: 1rem;">​ to see if I have ruby installed. I get a version returned, Great!! my mac has ruby installed so I should be able to just start developing. But No. Come to find out the system version preinstalled on the mac is not new enough, nor should I upgrade this version as it could break my mac. Of course in this day of </span>development<span style="font-size: 1rem;">, the solution was to install a package manager to install what I need. So I grabbed&nbsp;</span>`rbenv`<span style="font-size: 1rem;">​ to manage the ruby versions on my macbook. Commands ran to get this up and running:</span>

```
brew install rbenv

rbenv install 2.3.0

rbenv init
```

### Stage 2 - Pivoting to Hugo

As there was nothing wrong with Jekyll, I decided to learn something new and try out Hugo to see if there was anything I was missing

### Stage 3 - Hello Forestry

Loading in Forestry, oops I shared the same branch, migrating content.

### Stage 4 - Branching and Deploy Strategy

### Stage 5 - Removing Duplication w/ Shortcodes

### Appendix - Ongoing Development

Hope you enjoyed

-Sean Whalley