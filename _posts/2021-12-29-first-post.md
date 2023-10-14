---
layout: post
title:  "blogging with Jekyll"
date:   2021-12-30 10:46:00
categories: learning
---
<br />
I finally spent some time learning how to host my blog on Github using Jekyll, a Static Site Generator (SSG). This blog is using Jekyll.

It took me nearly 3 days during my winter break to learn Jekyll. Here were the hurdles and tips I learned along the way:

1. <b>Front Matter</b>
<br />
It is the first block of key-value pairs you see in a file that uses YAML, which configures files and is in between triple-dashes like so:

{% highlight ruby %}
---
layout: post
title: my blog
---
{% endhighlight %}

2. <b>File _config.yml</b>
<br />
This is one of the most important files since it is used to customize how your site is built. You can configure the settings in this file like the type of theme and plugins you want. 

While I wanted to use one of many customized Jekyll themes, it took me an endless amount of time googling and reading to figure out that all I needed to do was add the name of the theme in the form of the creator's name and their theme's github repo like so:

{% highlight ruby %}
remote_theme: rosario/kasper
{% endhighlight %}

Assuming I downloaded the Kasper theme files and dragged them in my working directory.

3. <b>Gemfile and Ruby</b>
<br />
This is essential for running Ruby programs. The `Gemfile` holds all the gems that you want to include in your project. It's used with bundler to install, update, remove, and manage your Ruby gem dependencies. 

Once you run the `bundle install` in the command line, a `Gemfile.lock` file will appear in your directory. It's like a vault where all the dependencies are stored. I had to delete it and run `bundle install` again since this website wasn't rendering locally at first. 

4. <b>Local file structure</b>
<br />
If you decide to use a customized Jekyll theme, the files you want to keep are Gemfile, _config.yml, _posts, _includes, _layouts, _sass, _site, assets, .jekyll-cache. The first two files can be configured. 

After organizing the files, you can start writing your content in _posts, where the files are in markdown or html extensions. Make sure the name of the file is in the following format:

{% highlight ruby %}
yyyy-mm-dd-fileName.md 
{% endhighlight %}

Here is the full [Jekyll](https://jekyllrb.com/docs/) documentation.

That wraps it up. I'm proud of myself for learning Jekyll and having a simple site up in the process. It was time well spent.

-- JK