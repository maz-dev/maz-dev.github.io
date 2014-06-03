---
layout: post
title: "Rails4 and Cancan"
date: 2014-06-03 22:35:49 +0200
comments: true
categories: Rails
---

How to overcome the ActiveModel::ForbiddenAttributesError
--------------------------

Usually when starting a rails project, I only had to manage a few users able to edit the content of the site. All the other interacting with this content but not handling it directly.

But this changed recently as I worked on Crassier, an open source app to manage local events (gigs, cinema etc..). The content’s editor is the user itself.

To deal with roles I used cancan, and this is awesome.

BUT I got a nasty error. ActiveModel::ForbiddenAttributesError ..

This issue is already known. See https://github.com/ryanb/cancan/issues/835

TLDR: Insert this block in your application_controller

{% codeblock lang:ruby %}
before_filter do
  resource = controller_path.singularize.gsub('/', '_').to_sym
  method = "#{resource}_params"
  params[resource] &&= send(method) if respond_to?(method, true)
end
{% endcodeblock %}