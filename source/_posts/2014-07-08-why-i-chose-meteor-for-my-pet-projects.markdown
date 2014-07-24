---
layout: post
title: "Why I'm picking meteor for my pet projects"
date: 2014-07-08 11:35:32 +0200
comments: true
categories: Meteor
---

Meteor is a *kind of* new node-realtime-publish/subscribe framework, you can check it [here](http://meteor.com/).

When I started working on Crassier a few months ago, I chose Rails as the foundation.
It is a solid framework, well tested, well documented and a pleasure to work with. **And oh Ruby I love you**.

But after 4 full years working with it, I felt like I needed to explore new things.
 I followed the hip mob and got my hands dirty with nodejs. Cool, async is nice,
 the ecosystem is nice, javascript is nice after you really learn to work with it.
 Express is like Sinatra, I like Sinatra.

But hey, where's my productivity? I'm working alone on Crassier and I need some real projects to learn new techno stacks.
 So I tried to reimplement it in Sails, express and even gave a try to loopback. I learned Emberjs, I love it so much.
 All these solutions requires a lot of boilerplate, except perhaps for Sails, which is getting at the quality level of Rails very quickly.

Then I decided to give meteor a try. I purchased the [discover meteor book](http://discovermeteor.com), followed the awesomely clear and well written project
tutorial. I had so much fun. This is a smart framework, created by smart people. I was about to give up on node, as I don't need extreme scaling for my pet projects,
 and here comes meteor. To put it simply, real time capability comes free with the framework, the front and the server can share a **LOT** of code and the templating and
 rendering engine is pretty nice.

Just by playing a little with it, I got a ton of new ideas to implement in Crassier.

*    A private chat system? Easy.
*    Reusable Inline editing system? Just a simple helper, 30 lines of code.
*    Live update on comments? Backed in the framework.
*    Layout and views system similar to angular/ember with reactivity? Backed in.

Auth system backed in, even with views and forms for login, sign-up etc. Lost password system? Ok we got that. Need Oauth? Backed in.

If you're missing a feature you can check [Atmosphere](https://atmospherejs.com), a package manager which is dead simple.
But trust me, implementing usual features is simple and straightforward in Meteor.

You can even use npm packages with a little effort. Just create a package file and done.

Well, you get the point. Meteor is simple, clean and smart. Ruby was created to maximise programmer happiness. Rails followed this moto.
It looks like Meteor adds the fun to the recipe.

The title states that I use meteor for my pet projects. For now I haven't really used it in production.
 There shouldn't be any big issue but I'll encounter some pitfalls for sure, mainly due to me being inexperienced with Meteor.
 When I'm ok with the prod setup, I'll surely consider it for some client work.

I'll do a follow up to this blog post once Crassier is online.

Now, if you're looking for the drawbacks I found using meteor :

*    Mongodb. Yep, take it or leave it. For crassier it's not a real issue as my data model is denormalized anyway.
*    Javascript. As I said, I like it. If you don't, you could try coffeescript.
*    Meteor API is not yet completely stable. You should inspect the changelogs on every release. But you do that anyway huh?
*    The main difficulty is to know what data to publish, without overpublishing. Not a drawback, but the paradigm change from other frameworks can slow you down.

And that's pretty much it.

[Crassier](https://github.com/maz-dev/crassier) is an events and artistic community app.
I will soon update it with the meteor version.

If you're feeling bored with your current framework, please give meteor a try.
 I do my job because I love to create things, Meteor allows me to do it in an exciting way. I'm still amazed by the ease of use of this framework.

 Infinite kudos to the meteor team and community.
