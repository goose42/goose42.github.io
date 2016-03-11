---
layout: post
title:  "I'm going to try this Jekyll thing"
date:   2016-03-10 18:58:17 -0800
categories: jekyll
---
Of late, I've felt the need to document things that I come across, that might have code samples in them. I also like the idea of typing things out on a text editor, instead of a web browser.

[Jekyll][jekyll-docs]{:target="_blank"} seems like the right tool for this job. So I'm going to try it for a while.

So how did I start with Jekyll? I stated [here][jekyll-gh]{:target="_blank"}. This is Github's documentation for setting up and hosting static pages on github.

I created this [repository][repo]{:target="_blank"}, and cloned it on to my local machine.

{% highlight bash %}
  $ git clone git@github.com:goose42/goose42.github.io.git
{% endhighlight %}
*(Sidenote: Doesn't this sample look so much better that it would on wordpress?)*

Once I had the repository, I installed and configured Jekyll. (I already am running ruby 2.3.0)

{% highlight bash %}
  $ gem install jekyll
  $ jekyll new . --force # --force, because the folder wasn't empty.
  $ jekyll serve
{% endhighlight %}

Now, when I navigated to `http://localhost:4000` on a browser, I was able to see the sample website that is created by Jekyll. The navigation is pretty straight forward and editing the `_config.yml` file in the application root directory, as well as the `.markdown`(:heart_eyes:) file in the `_posts` directory, I was able to create this post.

The `jekyll serve` command runs a server that is able to reload when ever I save changes to any markdown file, and if I simply refresh my browser tab, I am able to see the updated version of the post.

Now, I would like to publish this post, so I simply commit my changes my git repository and push them out to github.
(I thought I had to build the pages with `jekyll build`, but I did not need to. Perhaps I need to find out exactly exactly what that does.)

{% highlight bash %}
  $ git add _posts/2016-03-10-starting-jekyll.markdown
  $ git commit -am "My first post"
  $ git push
{% endhighlight %}

This should have published my changes to github, and I should be able to see this post on [live][home]{:target="_blank"}

Now that this was set up, I wanted to change the landing page to be an "about" section, and separately link to the actual blog. The details of this change can be tracked [here][commit1]. The short gist of it is, that I changed the `layout` attribute on the index page to be what was originally the about page, and created a `blog.md` file that would hold what was originally the `index.html` file.

Seems pretty straightforward so far. Maybe this could do well with themes? Maybe I could make my own theme. Will probably update this post as I have more information.

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://pages.github.com
[repo]:        https://github.com/goose42/goose42.github.io
[home]:        goose42.github.io
[commit1]:     https://github.com/goose42/goose42.github.io/commit/bb18a445eb8a047da389056545c9d94e7b4a8a98  
