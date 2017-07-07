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

During this process understanding that I needed a different version of ruby and getting installed was the biggest pain-point. Jekyll (along with Hugo) make things very easy to get all the boilerplate up and running. With all the complications of today's software world, I am so happy to see both companies took the time to create a nice clean interface to getting up and running fast.

Jekyll maintains a [quick start guide ](https://jekyllrb.com/docs/quickstart/)which is very simple to follow. After ruby was installed, I had a site up and running in less than 5 minutes. This was a great feeling to be up and running so fast.

Rolling a theme was easy in Jekyll as there was no boilerplate theme I had to cleanup and I could begin. Flexbox is a great CSS feature that makes div/float hell go away. No more inline blocks with offsetting 4 px tricks to get things to align properly. The markup ended up being very clean with only a `main.css`<span style="font-size: 1rem;">​ and&nbsp;</span>`responseive.css`<span style="font-size: 1rem;">​ file for mobile devices. The theme colors used were based on the PEI flag, so there was a bunch of green on the site.&nbsp;</span>

My biggest takeway from working with Jekyll were their `/_data/`<span style="font-size: 1rem;">​ folders. Being able to have the static content pulled out into simple&nbsp;</span>`.yml`<span style="font-size: 1rem;">​ files made it easy to maintain larger more dynamic parts of the application. Our site has a large Bio section for all of the elders past and present. The yml file helped remove a lot of duplication and I was create the data in a </span>separate<span style="font-size: 1rem;">&nbsp;file and iterate over the data. Removing the duplication, as some of you may know, is my favorite thing to do in code. Finding duplication and deleting code makes me happy.&nbsp;</span>

<span style="font-size: 1rem;">The site was coming along good but real life caught up to me and I had to shelf the project for a few months. If you have interest in seeing how the site looked when it was shelved you are welcome to check it out on my github page</span>

<span style="font-size: 1rem;">Source :&nbsp;</span><span style="font-size: 1rem;"><a href="https://github.com/swhalley/sampleJekyl">https://github.com/swhalley/sampleJekyl</a></span>

<span style="font-size: 1rem;">Demo:&nbsp;</span><span style="font-size: 1rem;"><a href="https://swhalley.github.io/sampleJekyl/">https://swhalley.github.io/sampleJekyl/</a></span>

### Stage 2 - Pivoting to Hugo

After a bit of time away from the development of the site I decided to learn something new and try out Hugo to see if there was anything I was missing

### Stage 3 - Hello Forestry

Loading in Forestry, oops I shared the same branch, migrating content.

### Stage 4 - Branching and Deploy Strategy

### Stage 5 - Removing Duplication w/ Shortcodes

### Appendix - Ongoing Development

Hope you enjoyed

-Sean Whalley