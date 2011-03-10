---
layout: post
title: Core skills
tags: [vim]
---

Lately I've been trying to focus on my core skills. Nothing is more essential to a programmer
than getting code written down and that is between your fingers and your editor.

In terms of fingers, I recently revisted (ok, visited for the first time) touch typing. This
was an experience for me since I could type decently fast, but was only using a subset of my
fingers to do so. I printed out and taped the
[fingering chart](http://upload.wikimedia.org/wikipedia/commons/2/29/Touch_typing.svg)
at my desk at work and at home and even switched to a natural keyboard to enforce the
correct hands for the middle keys.

The result? I now use more of my fingers and I can use natural keyboards, but I wouldn't say
I'm a pure touch typer. I think that overall my speed has improved and is slightly improving
as I go along. At least my ring fingers have more to do now.

In terms of my editor, I use (g)vim and have been trying to learn more and more about how to
make it work for me. Part of this is collecting the right plugins and writing a config that
works with you to use those plugins. To that effort, I reconsolidated my .vim directory
to use gitsubmodules and pathogen and put it up on [github](https://github.com/zbelzer/dotvim).
I modeled it after [this post](http://tammersaleh.com/posts/the-modern-vim-config-with-pathogen)
by Tammer Saleh and have found it extremely easy to manage.

One of the most useful things about setting your configuration up this way is that I can go
to a box, whether it's a remote machine or a friend's who doesn't use vim and simply run:

{% highlight sh %}
$ ruby .vim/install.rb
{% endhighlight %}

and it will symlink (with prompts when replacing) .vim and .gvim into your home folder as well
as initialize the submodules and compile CommandT.

I've found between the plugins I've decided to use and mnemonic style leader mappings, I've
been able to vastly increase my productivty. This is mostly due to my newfound ability to open
a project and dive into the code with ease. This is especially useful for ruby gems.

If you use vim, I'd highly suggest this approach. Also, check out [Vimcasts.org](http://vimcasts.org)
to learn some new tricks and techniques.
