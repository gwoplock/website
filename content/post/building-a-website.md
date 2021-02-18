---
title: "Building a Website as a Firmware Developer"
date: 2020-06-10
description: "The struggles of building a website without any knowledge"
author: "Garrett"
draft: true
categories: "Programming"
tags: ["webdev"]
---

If you haven't guessed from the title I'm not well versed in building websites. In fact, this is really the first website I've made "from scratch" and even this isn't really a from-scratch website.

This adventure started when a friend, John, built a site to house his [blog](https://ptcrash.dev). I had wanted to start blogging but for one reason or another, I wouldn't. Id open medium or dev.to or whatever log in and look at the blank page and freeze. Once he started I said I'll start blogging too. I figured if I sunk cost before actually writing a post I could force myself to write the posts. We'll see how that works out.

John had used a static site generator, [Hugo](https://gohugo.io/), and hosted it on GitHub pages. If you haven't noticed the footer, I followed suit. After reading the docs I figured how hard could it be and make my site. And it was really as easy as the quick start guide made it seem. But that's where it stopped.

After following the guide I figured I'd make a post to test out the main feature I needed. A quick command later, the date and time for the post was wrong but who cares that's easy to fix. I think that was a bug in the theme but whatever. I fixed the date and my post didn't show up. what... It made no sense, Hugo didn't generate the paged, directories, front page listing or anything. I figured the simplest thing to do was to make sure the theme worked so back to the quick start guide I went and grabbed the theme they said to use. Still nothing, double what... I made a new blog post and that worked. Sure whatever Hugo. After coping different bits of the front matter I figured out I must have change the date to be the wrong format. A little warning would be nice.

Ultimately this was weird, I was building a "program" but I really wrote no code. A config file and some markdown, I could get used to this kind of webdev. But then it happened, I wanted to give credit and add the CC disclaimer to the footer, the theme didn't do that. I felt like this would be a problem but it really wasn't. I was able to open up the theme and make the changes I needed to. It didn't even really require HTML. 

I have had some experience building web sites, at my job for a while I was a full-stack developer. I hated it, I hated fighting CSS, I hated the 8 million ways of doing anything, I hated versioning, I hated it. Maybe it's because I'm used to telling a computer to do something and it does it, but that's not the case on the internet. maybe it was because of the tooling. Whatever the reason it left a bad taste in my mouth. Hugo was a breath of fresh air, I was able to spin up a site quickly. I didn't have to worry about styling or layout or design or components or anything. I was able to get right down to brass tacks and build a website. Plus if I want to add a feature it isn't that hard. 

Hugo didn't completely change my mind about webdev, I still want to be a firmware developer. But if someone asks (and pays) for a simple site, I'd think twice before turning them down

--Garrett