---
layout: post
title: "Joins in Meteor"
date: 2014-07-24 11:35:32 +0200
comments: true
categories: Meteor
---

Joins in meteor are not a big deal, but you have to make them reactive.
You can overpublish, denormalize or just do it the right way with a reactive publish.

I'm using a package to do this for me, ["Publish composite"]("http://atmospherejs.com/package/publish-composite").

Of all the packages helping you to make your publications reactive, this is the one that I got to work easily.
