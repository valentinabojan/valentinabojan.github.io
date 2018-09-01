---
layout: post
title: How to create a blog using GitHub Pages and Jekyll in 1 day
tags: [Blogging, Howto]
---

What should my first post be about if not about this blog genesis?

GitHub Pages and Jekyll were the choice to be the foundation of this blog,
but there were a lot of bit and pieces that polished it.

<!--- excerpt -->

Did this choice worth it? Completely! Any engineer would understand the choice. 
We love the challenges, the puzzles, the ups and downs when building something.
Tell an engineer that he could choose between having a website just 1 click away, or manually configuring it as he likes, getting dirty to add features that he needs. 
The answer talks by itself. Oh, we love getting dirty. 😉

## Set the blog foundation

<dl>
    <dt>1. Start your blog using GitHub Pages</dt>
    <dd>
        <a href="https://pages.github.com">Here</a>
        you will find how to link your GitHub repository to your new public website.
    </dd>
    <dt>2. Choose a Jekyll theme</dt>
    <dd>
        This blog uses the 
        <a href="http://lanyon.getpoole.com">Lanyon</a>
         that gives you a basic blog out of the box.
    </dd>
</dl>


## Make you blog ready to meet the world

Even if you can start writing posts, your blog is not as shinny as you imagined it. But it can be... 

**1. Configure your contact list** 

If you started writing a blog, for sure you worked in a lot of other interesting projects. Use your blog to share your contributions to the community.

The sidebar can a very good place to gather your contact list.
You can use a minimalistic way to hint them, by using [Font Awesome](https://fontawesome.com).

Just load the stylesheet in your *head.html* file and start using them in your *sidebar.html* file.

<!--
{% highlight html %}
<head>
  ...
    
  <!-- Icons -->
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.2.0/css/all.css" integrity="sha384-hWVjflwFxL6sNzntih27bfxkr27PmbbK/iSvJ+a4+0owXq79v+lsFkW54bOGbiDQ" crossorigin="anonymous">

  ...
</head>
{% endhighlight %}

{% highlight html %}
{% raw %}
<div class="sidebar" id="sidebar">
  ...
  <div class="sidebar-item content-center">
    <a href="{{ site.author.github }}">
      <i class="fab fa-github-square fa-2x"></i>
    </a>
    <a href="{{ site.author.linkedin }}">
      <i class="fab fa-linkedin fa-2x"></i>
    </a>
    <a href="mailto: {{ site.author.email }}">
      <i class="fas fa-at fa-2x"></i>
    </a>
  </div>
  ...
</div>
{% endraw %}
{% endhighlight %}
-->

**2. Add reading time**

You could help your readers by listing the estimated reading time of a blog post.
This way, they will decide if that's the time to read the post or if they should postpone it for later.

[Here](http://atekihcan.github.io/blog/2014/reading-time-estimate-in-jekyll/)
you can find a very good example of how to compute the reading time based on the post content length.


**3. Create drafts for your posts before publishing them**

Don't hesitate versioning your post drafts.
You can safely do this by putting your draft files in a *_drafts* directory.

GitHub Pages will know how to deal with the *_drafts* content and not publish it.
Locally you can always preview your drafts by running the `jekyll` command with the `--drafts` flag: `jekyll server --watch --drafts`

When your post is ready, just move it in the *_posts* directory.


**4. Add post excerpts in the Home page**

By default, the Lanyon theme shows all posts (paginated of course) in your blog *Home* page.
If you want to change this behavior and display only a post teaser instead, you should configure the so called *post excerpts*.

For this, you'll have to choose a excerpt separator and specify it in the *_config.yaml* file.

{% highlight yaml %}
excerpt_separator: '<!-- excerpt -->'
{% endhighlight %}

To display the post excerpts instead of the contents, you'll need to modify the *index.html* file accordingly.
{% highlight yaml %}
{% raw %}
// replace this
{{ post.content }}

// with this
{{ post.excerpt }}
{% endraw %}
{% endhighlight %}

Then, when writing your post you will manually use the excerpt separator in the place where you want your post teaser to stop.


**5. Monitor your website traffic with Google Analytics**

[Google Analytics](https://analytics.google.com) can prove to be a very good toll to better understand your readers.
Apart from tracking the visualisation number of your blog, you can use Google Analytics to see
the pages that are visualised the most, when are blog posts most visited, how much time the readers spend accessing your blog.

Based on these details, you can decide what to write next.

You can follow [this blog post](https://desiredpersona.com/google-analytics-jekyll/) to configure Google Analytics for your new website.




**6. Change the post date format**

In case you don't like the default date format for your posts (i.e. *date_to_string*, e.g. *03 May 2013*), you can easily change it 
by configuring your preferred format.

Check [this post](http://alanwsmith.com/jekyll-liquid-date-formatting-examples) for more examples. 

