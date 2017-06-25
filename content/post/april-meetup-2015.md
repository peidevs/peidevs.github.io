+++
categories = []
date = "2015-04-15T00:00:00Z"
description = ""
tags = []
thumbnail = ""
title = "April Meetup 2015"

+++
Our April meetup is behind us and the group continues to grow. April was the largest meetup to date as we had 33 people in attendance. Some of you may not have been aware but this was the 3rd anniversary of the PEIDevs group. The group was started by Dustin Sparks in April 2012. Through word of mouth and quality talent we are happy to see where the group can go in the future.

For the April meetup we had two speakers. Derek Campbell (@[derekscampbell1](https://twitter.com/derekscampbell1)) talking about Managed Development Environments and Ryan Palmer (@[rypalmer](https://www.twitter.com/rypalmer)) talking about Travis CI.

**Derek Campbell**

Derek kicked off our evening trying to solve the age old problem “Well it worked on the developers machine”. He discussed how Code and Environmental Pollution can cause problems as code and systems work differently depending on the environment they are run in.![](/uploads/2017/04/24/derek__.jpg)

Derek explored 4 different products which can help solve these problems

**Virtual Machines** - Virtual machines allow you to setup many different environments for your work. This helps prevent multiple projects from stepping on each other as they can each be managed in their own VM. Storing them in their own VM makes for quick switching between tasks.

**Vagrant** - If you have many people working on a project at the same time ensuring they all setup their VM the same is a tough task. Vagrant makes managing Virtual Machines easier. Vagrant configuration files can be stored in source control rather than large base images.

**Packer** -  Packer solves the problem of building new base images. Packer is configuration based so new and entire environments can be created with configuration files. Packer uses JSON for its configuration files. So a lot of developers will already be familiar with the syntax.

**Docker** - Docker is harder to explain so we will let the company that builds the product define it: “The Docker Engine container comprises just the application and its dependencies. It runs as an isolated process in userspace on the host operating system, sharing the kernel with other containers. Thus, it enjoys the resource isolation and allocation benefits of VMs but is much more portable and efficient”.

**Ryan Palmer**

The second talk of the evening was on Continuous Integration. Ryan Palmer talked about his experiences using Travis CI.![](/uploads/2017/04/24/ryan_april.jpg)

Travis CI is a hosted solution that is free for open source projects to run their unit tests on. Ryan discussed how the environment is pluggable and anything else required can be scripted to make it work. There was support for most of the popular programming languages which gives it a wide range of support.

Since the system is pluggable there was support for many popular configurations such as integration with Headless browser testing (i.e. Selenium), postegres or memcache.

Ryan mentioned that one of his favorite features was the notification engine which allowed you to configure many different ways to get the outcome of the build. You can integrate with email and text message which most are used to. But Travis CI also has support for IRC or HipChat which allows the CI environment to communicate directly with your team without filling up your in box.

In the demo, Ryan showed us how Travis could be setup to test against different versions of a language in order to test for past and future support. One of the examples he gave showed testing his application against 5 versions of Phython to ensure that whatever the user had on their system, the tests would pass. There was no need to setup different CI environments to do this. It could be done all within the same environment and controlled via a configuration file.

Good talks from both of our speakers!!

**Scooter**

After the event we had a demo showing off PEIDevs first ever open source project, Scooter. Scooter is the brain child of Michael Easter and collaborated on by Evan Porter and Sean Whalley.

Scooter is an open source project hosted on the [PEIDevs GitHub Repo](https://github.com/peidevs) which is used to help perform the duties of picking our door prize winners. It was written in Dojo (Javascript framework) using the [WebStorm IDE](http://www.jetbrains.com/products). Feel free to perform fork and crate pul requests to help out.

Scooter is inspired by the stage hand of the Muppets. Can you see the similarities?![](/uploads/2017/04/24/scooter.png)

A BIG THANK YOU to our sponsors who make these events happen.

* JetBrains
* BinaryStar
* ScreenScape
* Michael Easter

We had a few prizes to give out at this event. And of course scooter was used to determine the winners. Congratulations to:

**Callista Tan **who won a box set of Estimotes courtesy of [Estimote.com](http://estimote.com/), **Ross Evans** who won a Amazon.ca $50 Gift Card courtesy of [Kelly Lantz](http://www.century21.ca/kelly.lantz). **Mark Wright** won the big prize of the night. A JetBrains licence which he redeemed for a copy of IntelliJ IDEA. Thank you to JetBrains for providing the licence.





