---
layout: post
title: How to create a blog using GitHub Pages and Jekyll in 1 day
tags: [Blogging, Howto]
---

What should my first post be about if not about the genesis of this blog?

GitHub Pages and Jekyll were the choice to form the foundation of this website,
but there were a lot of bits and pieces that polished it.

<!--- excerpt -->

Did this choice worth it? Completely! Any engineer would understand the choice. 
We love the challenges, the puzzles, the ups and downs when building something.
GitHub Pages and Jekyll give you the chance to manually configure your blog as you like and get dirty when adding the features that you need. 
Oh, we love getting dirty. 😉

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


## Make your blog ready to meet the world

Even if you can start writing posts, your blog is not as shiny as you imagined it. But it can be... 

**1. Configure your contact list** 

If you started writing a blog, for sure you worked in a lot of other interesting projects. Use your blog to share your contributions to the community.

The sidebar can a very good place to gather your contact list.
You can use a minimalistic way to hint them, by using [Font Awesome](https://fontawesome.com).

Just load the stylesheet in your *head.html* file:

{% highlight html %}
<head>
  ...
    
  <!-- Icons -->
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.2.0/css/all.css" integrity="sha384-hWVjflwFxL6sNzntih27bfxkr27PmbbK/iSvJ+a4+0owXq79v+lsFkW54bOGbiDQ" crossorigin="anonymous">

  ...
</head>
{% endhighlight %}

and start using them in your *sidebar.html* file:

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


**2. Add reading time**

You could help your readers by listing the estimated reading time of a blog post.
They will use it to decide if that's the time to read the post or if they should postpone it for later.

[Here](http://atekihcan.github.io/blog/2014/reading-time-estimate-in-jekyll/)
you can find a very good example of how to compute the reading time based on the post content length.


**3. Create drafts for your posts before publishing them**

Don't hesitate versioning your post drafts.
You can safely do this by putting your draft files in a *_drafts* directory.

GitHub Pages will know how to deal with the *_drafts* content and not publish it.
Locally you can always preview your drafts by running the `jekyll` command with the `--drafts` flag: `jekyll server --watch --drafts`

When your post is ready, just move it in the *_posts* directory.


**4. Add post excerpts in the Home page**

By default, the Lanyon theme shows all posts (with their entire content) in your blog *Home* page.
If you want to change this behavior and display only a post teaser instead, you need to configure the so called *post excerpts*.

For this, you'll have to choose an excerpt separator and specify it in the *_config.yaml* file.

{% highlight yaml %}
excerpt_separator: '<!-- excerpt -->'
{% endhighlight %}

To display the post excerpts instead of the contents, you'll need to change the *index.html* file accordingly.
{% highlight yaml %}
{% raw %}
// replace this
{{ post.content }}

// with this
{{ post.excerpt }}
{% endraw %}
{% endhighlight %}

Then, when writing your post you will manually use the excerpt separator in the place where you want your post teaser to stop.

**5. Change the post date format**

In case you don't like the default date format for your posts (i.e. *date_to_string*, e.g. *03 May 2013*), you can easily change it 
by configuring your preferred format.

Check [this post](http://alanwsmith.com/jekyll-liquid-date-formatting-examples) for more examples. 

**6. Monitor your website traffic with Google Analytics**

[Google Analytics](https://analytics.google.com) can prove to be a very good tool to better understand your readers.
Apart from tracking the views count of your blog, you can use Google Analytics to see
the pages that are visualised the most, when are blog posts most visited, or how much time the readers spend on your blog.

Based on these details, you can decide what to write next.

You can follow [this blog post](https://desiredpersona.com/google-analytics-jekyll/) to configure Google Analytics for your new website.


**7. Enable Disqus comments**

You will want to keep in touch with your readers, receive suggestions and  offer support when there are any questions.
Enabling post comments can help you in this regard.

[Disqus](https://disqus.com) is a good tool for this. Create an account and follow their instructions to enable comments for your blog posts.

Add the new Disqus information in the *config.yaml* file:

{% highlight yaml %}
{% raw %}
# Example
disqus-id: <your-disqus-id>
{% endraw %}
{% endhighlight %}

Load Disqus comments using this *comments.html* file:

{% highlight html %}
{% raw %}
<div id="disqus_thread"></div>
<script>
    var disqus_config = function () {
        this.page.url = "{{ site.url }}{{ page.url }}";
        this.page.identifier = "{{ site.disqus-id }}{{ page.url | replace:'index.html','' }}";
    };

    (function() { // DON'T EDIT BELOW THIS LINE
        var d = document, s = d.createElement('script');
        s.src = "https://{{ site.disqus-id }}.disqus.com/embed.js";
        s.setAttribute('data-timestamp', +new Date());
        (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
{% endraw %}
{% endhighlight %}

Include comments in the posts layout:

{% highlight html %}
{% raw %}
<div class="post">
  <h1 class="post-title">{{ page.title }}</h1>
  {{ content }}
  {% include comments.html %}
</div>
{% endraw %}
{% endhighlight %}

To display the number of comments for your posts, load the following script in your *default.html* file:

{% highlight html %}
{% raw %}
<script id="dsq-count-scr" src="//{{ site.disqus-id }}.disqus.com/count.js" async></script>
{% endraw %}
{% endhighlight %}

Display the number of comments in your *post.html* file:

{% highlight html %}
{% raw %}
<div class="post">
  <h1 class="post-title">{{ page.title }}</h1>
  <span class="post-date">
    <i class="far fa-comment-dots"></i>
    <a href="{{ site.url }}{{ page.url }}#disqus_thread" data-disqus-identifier="{{ site.disqus-id }}{{ page.url | replace:'index.html','' }}">Join the discussion</a>
  </span>
  {{ content }}
  {% include comments.html %}
</div>
{% endraw %}
{% endhighlight %}


**8. Add tags**

You can annotate your posts with one or more tags and allow this way grouping them by category.
This way, if your readers are interested in a certain subject, they can easily view all posts related to it.

To have this feature, start by adding tags to each one of your posts. For example, like this:

{% highlight yaml %}
---
layout: post
title: How to create a blog using GitHub Pages and Jekyll in 1 day
tags: [Blogging, Howto]
---
{% endhighlight %}

For every post, dynamically display the tags in the *posts.html* layout: 

{% highlight html %}
{% raw %}
<div class="post">
  <h1 class="post-title">{{ page.title }}</h1>
  <span class="post-date">
    {% if page.tags != empty %}
      <i class="fas fa-tags"></i>
      {% for tag in page.tags %}
        <a href="{{site.baseurl}}/tags/#{{tag|slugize}}">{{ tag }}</a>
      {% endfor %}
    {% endif %}
  </span>
  {{ content }}
</div>
{% endraw %}
{% endhighlight %}
 

Add a link to the new *Tags* page in the *sidebar.html* file:

{% highlight html %}
{% raw %}
<a class="sidebar-nav-item" href="{{ site.baseurl }}/tags">Tags</a>
{% endraw %}
{% endhighlight %}

Create a new *tags.md* file and reference the *categories* layout:

{% highlight yaml %}
---
layout: categories
title: Tags
---
{% endhighlight %}

Create the corresponding *categories.html* layout file:

{% highlight html %}
{% raw %}
---
layout: default
---

<div>
  {% for category in site.tags %}
  <div>
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <h3 class="category-head">{{ category_name }}</h3>

    <ul style="list-style-type:none">
    {% for post in site.tags[category_name] %}
      <li><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></li>
    {% endfor %}
    </ul>
  </div>
  {% endfor %}
</div>
{% endraw %}
{% endhighlight %}

**9. Enjoy your new blog 🍺**
