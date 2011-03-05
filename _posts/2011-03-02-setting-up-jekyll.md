---
layout: post
title: Setting up Jekyll
tags: [ruby, jekyll, github]
---

So I set up a new blog, which is pretty ordinary these days. I'd say most tech guys like me already
have one, but that would be a lie as I don't know of a single co-worker who does. I figured that
since I'd like to talk about technical things I'm doing that starting with the blog engine I'm using
would be fitting. Here goes.

[Jekyll](https://github.com/mojombo/jekyll) is a lightweight blogging engine based out of a git project. Essentially, every time you
make changes like adding a page or changing some styling you need to 'build' your site. This creates
the appropriate html pages as well as supplemental information like a sitemap and RSS feed. To start,
you need to get the Jekyll Gem.

{% highlight sh %}
$ gem install jekyll
{% endhighlight %}

I didn't want to have to start from complete scratch when creating my site, so I used
[Kris Brown's](https://github.com/krisb/jekyll-template) template.

{% highlight sh %}
$ git clone https://github.com/christianhellsten/jekyll-template.git blog
{% endhighlight %}

This template comes with a few extra conveniences, most notable are SASS, jQuery, Google Analytics and Disqus.
The configuration for these can be found in `_config.yml`. Start your local Jekyll webserver with 
`jekyll --auto --server`. It will compile the site automatically as you make changes. I then proceeded to 
update the HTML and SASS to my liking. Use `compass watch` to avoid having to rebuild your SCSS into CSS all the time.

Once you're ready to see it live, deploy it to github. To do this, all you need to do is initialize your project and
push it to a repo in your account called \<login\>.github.com. In my case, this is zbelzer.github.com. From within
your projcet, do:

{% highlight sh %}
$ git init
$ git remote add origin git@github.com:<login>/<login>.github.com
$ git push origin master
{% endhighlight %}

Github will build your site for you and send you an email.
