---
layout: post
title:  "How do I create a ruby gem?"
date: 2014-06-21 15:40:09 -0400
comments: true

---

## Background
Last week, I pulled a file out of my lib directory of a project because I thought that we might try and use it in another project.  I really want to prevent a copy paste situation.  So this led me to think about, how did I do this 8 months ago?

## 0. Before You Start
* Create a RubyGems.org account
* Make sure to query the name of your gem, to see if it already exists


## 1. gem install bundler  ![Mou icon](https://avatars1.githubusercontent.com/u/1137638?s=50)
Bundler will do most of the heavy lifting.  Pick a name for your gem and run...

{% highlight ruby %}
bundle gem my_gem
{% endhighlight %}

Now you should have a directory with your gem name and it contains all of the necessary file needed to start your gem.

## 2. Build Time
If you run 'rake -T' in the terminal, you will see...

{% highlight ruby %}
rake build    # Build my_gem-0.0.1.gem into the pkg directory
rake install  # Build and install my_gem-0.0.1.gem into system gems
rake release  # Create tag v0.0.1 and build and push my_gem-0.0.1.gem to Rubygems

{% endhighlight %}

Run these commands:

* rake build #to build your gem
* rake install #just to make sure your gem installs without issue

## 3. Release my_gem

When the gem is ready for release to RubyGems.org

{% highlight ruby %}
rake release
{% endhighlight %}

The first time you do this, you will be asked for your RubyGems.org credentials.

## Done
