+++
categories = []
date = "2017-07-07T13:36:00-03:00"
description = ""
tags = []
thumbnail = ""
title = "New PEI Devs Website"

+++


In July 2015 the group determined we should have some web presence to create a compilation of all of our resources in one area. [Michael](https://twitter.com/codetojoy) stepped up and created us a very simple bootstrap website with all of the resources jammed on the site to have the single source of information we desired.

We knew this was never going to be a long term solution and started thinking about what we wanted for a website. September of 2015 an [issue](https://github.com/peidevs/peidevs.github.io/issues/2) was logged to start revamping to have a proper website. <span style="font-size: 1rem;">Around this time we met the folks at </span><a href="https://forestry.io/" style="font-size: 1rem; background-color: rgb(255, 255, 255);">Forestry.io</a><span style="font-size: 1rem;"> who introduced us to static website generators </span><a href="https://jekyllrb.com/" style="font-size: 1rem; background-color: rgb(255, 255, 255);">Jekyll</a><span style="font-size: 1rem;"> and </span><a href="https://gohugo.io/" style="font-size: 1rem; background-color: rgb(255, 255, 255);">Hugo</a>

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

Rolling a theme was easy in Jekyll as there was no boilerplate theme I had to cleanup and I could begin. Flexbox is a great CSS feature that makes div/float hell go away. No more inline blocks with offsetting 4 px tricks to get things to align properly. The markup ended up being very clean with only a `main.css`<span style="font-size: 1rem;">​ and&nbsp;</span>`responsive.css`<span style="font-size: 1rem;">​ file for mobile devices. The theme </span>colors<span style="font-size: 1rem;">&nbsp;used were based on the PEI flag, so there was a bunch of green on the site.&nbsp;</span>

My biggest takeaway from working with Jekyll were their `/_data/`<span style="font-size: 1rem;">​ folders. Being able to have the static content pulled out into simple&nbsp;</span>`.yml`<span style="font-size: 1rem;">​ files made it easy to maintain larger more dynamic parts of the application. Our site has a large Bio section for all of the elders past and present. The yml file helped remove a lot of duplication and I was create the data in a </span>separate<span style="font-size: 1rem;">&nbsp;file and iterate over the data. Removing the duplication, as some of you may know, is my favorite thing to do in code. Finding duplication and deleting code makes me happy.&nbsp;</span>

<span style="font-size: 1rem;">The site was coming along good but real life caught up to me and I had to shelf the project for a few months. If you have interest in seeing how the site looked when it was shelved you are welcome to check it out on my github page</span>

<span style="font-size: 1rem;">Source :&nbsp;</span><span style="font-size: 1rem;"><a href="https://github.com/swhalley/sampleJekyl">https://github.com/swhalley/sampleJekyl</a></span>

<span style="font-size: 1rem;">Demo:&nbsp;</span><span style="font-size: 1rem;"><a href="https://swhalley.github.io/sampleJekyl/">https://swhalley.github.io/sampleJekyl/</a></span>

If you want to run the site locally, feel free to pull the code down yourself and follow the direction in the readme file from the source link.

### Stage 2 - Pivoting to Hugo

After a bit of time away from the development of the site I decided to learn something new and try out Hugo to see if there was anything I was missing. In April 2017 we started with Hugo. Using the [quickstart guide](https://gohugo.io/overview/quickstart/) for Hugo I had a site, with theme setup in 10 minutes. 8 of which was spent looking through [themes](https://themes.gohugo.io/), the other 2 watching the quickstart video.

```
brew install hugo
hugo new site peiDevs

```

I downloaded a theme ([mainroad](https://themes.gohugo.io/mainroad/)) and plunked it in the /themes/ folder, updated the Hugo config (`theme = "mainroad"`)  to point to the new theme and voila the site was up and running.

I chose mainroad as it was simple and had all of the components on the screen I was looking for. What I like about the way Hugo is setup is that we can pickup, throw away the old theme and grab another if we don't like the look without losing any content. The separation of content and theme is wonderfully done.

### Stage 3 - Hello Forestry

Now that the site was up and running I set out to complete the task of consolidating all of our links, old blogs and photos into the new site. This is where forestry came in handy. I was able to copy and paste old blogs into the posts section of forestry without having to worry about losing any formatting. The entire process took about two hours and the only thing I had to manually re-create were tweets. The copy process copied the text instead of the link to the tweet. This is expected and if I wanted more I could have looked at a migration tool. Instead I did this manually one night while watching T.V.

While editing posts I had access to both a wysiwyg editor for the raw copy/paste operations and when I needed more power the raw markdown was available to me.

When the migration was completed, the next step was to setup some of our boilerplate pages. Our [About](http://peidevs.github.io/about/) and [Code of Conduct](http://peidevs.github.io/code/) Pages were up next. Again the editors came in handy for these pages. We were able to delegate the tasks of getting this content written and it all came together pretty quickly. Members of the elder group stepped up to proofread documents and write their Bios. Some came in via Slack and others via Pull Requests and I was able to quickly pull these into the codebase via Forestry.

Forestry allowed me to create our navigation menus and manage their order and content easily. The site contained two menus which are now easily updated via anyone with access to our account.

During the process, the team at Forestry were very responsive in helping out answer questions as well as taking suggestions and feedback about my experience.

My big oops moment with Forestry came when I accidentally set both my source code branch and deploy location to be the same branch in github. When I clicked publish for the first time it overwrote a lot of content and I had to recreate the repository. Luckily I had not pulled down the changes so I was able to repoint my remote origin location. Nuke the remote repository and recreate things without any lose.

### Stage 4 - Branching and Deploy Strategy

Now that the development side of things were stable and most of the content was created or migrated it was time to think about how we would deploy and keep the site updated.

Our main site is located at [peidevs.github.io](https://peidevs.github.io) using an organization site with github. We were looking to retain that URL and needed a way to deploy there easily. Github uses a branching strategy where normally your source code lives in master/develop branch and you use a `gh-pages` branch to display your site. with the organization site, the `master` branch is where the content is served. This meant we needed another branch or repository to host our source code. Without thinking about this too much I created a `develop`<span style="font-size: 1rem;">​ branch to host the source code and then build the code from there. The manual steps to build were a bit of a pain.</span>

```
hugo
copy public/ /temp/
git checkout master
copy /temp/ .

```

In the above steps we build the site using hugo, copy the generated site out to a temp directory, checkout the master branch and then copy the files back to master. When you think of branches you generally think they should be hosting similar code but in our case, develop was the source and master is the generated site. They act as different repos. This may not be ideal but we can chalk this one up to some tech debt we can fix later.

I wanted a better way to generate the site then doing it manually every time. I looked at setting up TravisCI or CircleCI to auto deploy for me. But then I remembered that I had Forestry.  I setup my hosting to point to the master branch as my hosting for github pages and All worked well.

![](/uploads/2017/07/07/Screen%20Shot%202017-07-07%20at%202.13.02%20PM.png)

Now with the push of a button in Forestry, I can manage content or push development builds. This part has worked nicely so far now that it is setup.

### Stage 5 - Removing Duplication w/ Shortcodes

As part of the new site we wanted to introduce everyone to our [Elders](https://peidevs.github.io/about/#elders) as many of you may not know who we are. There are many new faces each month and it is hard to re-introduce ourselves all the time.

While creating the markdown file for the about page we ran into a scenario where we had duplicate html content for our elders. Each elder that is added to the list had duplication in the mark and if we ever decide to change the format of the site it wouldn't be easy to change all of them. Past and present there have been 12 elders. Duplicating this markup is expensive. Each elders Bio looked similar to

```
&lt;article class="loop__item post clearfix"&gt;
   &lt;figure class="loop__thumbnail"&gt;
      &lt;img src="member_159531172.jpeg"&gt;
   &lt;/figure&gt;
   &lt;div class="loop__content clearfix"&gt;
      &lt;strong&gt;Sean Whalley&lt;/strong&gt; - Sean has been part of the group since the 2nd meetup. He has helped organize ...
   &lt;/div&gt;
&lt;/article&gt;

```

Markdown doesn't really allow for easy manipulation to remove the duplication. I tried using frontmatter to create loops and generate the content. But that isn't processed by Hugo for Markdown files when the site is generated. This just spit code out on the screen instead of rendering our Bios.

I was introduced to [shortcodes](https://gohugo.io/extras/shortcodes/) when I was migrating the blogs over and needed to embed tweets into the blog posts. Shortcodes allow you to hide markdown and provide just the data need for a tag.

This takes the id of the tweet and when Hugo generates the site it auto converts it to the proper markup needed to display a tweet properly.

So I setoff on an adventure to create my own shortcode for Elders. The directions were not too complicated. Create an html file under `/layouts/shortcodes` and put all your markup required in that file and then use your shortcode. No extra configuration, Hugo is able to pick it up.

So I created a file called `elder.html` with the following content.

```
&lt;article class="loop__item post clearfix"&gt;
   &lt;figure class="loop__thumbnail"&gt;
      &lt;img src='{{ .Get "img" }}'&gt;
   &lt;/figure&gt;
   &lt;div class="loop__content clearfix"&gt;
      &lt;strong&gt;{{ .Get "name" }}&lt;/strong&gt; - {{ .Get "desc" }}
   &lt;/div&gt;
&lt;/article&gt;

```

This allows me to do some variable replacement as I can pass in name, img and desc to generate the markup for the page. My about.md file was then able to remove a lot of duplication. Instead of having all the html in the markdown file, I could simply call the shortcode

```
{{ &lt; elder 
  name="Sean Whalley"
  img="member_159531172.jpeg"
  desc="Sean has been part of the group since the 2nd meetup. He has helped organize ..."
}}

```

First run was a disaster. After starting up the site after first use I was greeted with the error

<blockquote>
<p>unable to locate template for shortcode "elder" in page "about.md"</p>
</blockquote>

This turned out to be a [bug](https://github.com/gohugoio/hugo/issues/3340) in the version of Hugo I was using. I promptly upgraded Hugo (`brew upgrade`) from `0.20.2`<span style="font-size: 1rem;"> to&nbsp;</span>`0.22.1`<span style="font-size: 1rem;"> and like any upgrade in an early release, I was expecting the worse. Breaking changes etc. But the upgrade was clean and easy. I repointed forestry to use the newer version of Hugo in their configuration menu and everything just worked.</span>

<hr>

<span style="font-size: 1rem;">At this point we are at today. We are still logging and fixing some issues but the site is stable.&nbsp;</span>

<span style="font-size: 1rem;">That is the adventure of the new site, h</span><span style="font-size: 1rem;">ope you enjoyed</span>

-Sean Whalley