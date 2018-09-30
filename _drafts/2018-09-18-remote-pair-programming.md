---
layout: post
title: Challenges when doing remote pair programming and how to overcome them
tags: [eXtreme programming, DevOps practices]
---

Known not only as one of the 12 practices of [Extreme programmin](https://ronjeffries.com/xprog/what-is-extreme-programming/),
but also as one of the DevOps practices that increases the quality of every development team work, pair programming is a technique 
that becomes more and more popular every day.

Doing pair programming doesn't sound difficult, but this doesn't mean there are no challenges to face in order to feel its benefits.
There are challenges, especially if we try to apply this practice remotely when working in distributed teams.

<!--- excerpt -->

## What is pair programming?

Pair programming can be shortly described as two programmers working together to solve a task, using a single computer. 

> *Wait! Four hands and only one keyboard?*

I know this can sound wrong for some of you, but when doing pair programming, we have roles that we have to take care 
to switch rather often, as following:
* **driver** - the person that actually writes the code
* **navigator** - the person that observes the driver and reviews the code as it is being written 

> *Wait! So two programmers are doing the same task? This sounds rather inefficient!*

Don't fall into this trap! Give it time to see its benefits! It may be that at first a pair finishes the task almost in 
the same time a single programmers does. But the code quality is undoubtedly better.

> *So two heads really are better than one!*

Yes! Working in pair, you will have the code reviewed by two programmers, a task that was implemented having a **better 
design**, a **better code quality** and that was **better tested** than it would have been if it was implemented by a single programmer.

As I mentioned earlier, the benefits will not appear immediately. As time passes, you will
notice that the **knowledge sharing inside the team is done quicker** than before applying pair programming.
Instead of asking around when you don't know certain areas from your project, start pairing with someone that does.
After one or two days of pair programming, instead of lacking information, you will be the one able to share information to someone else.

This practice can be **perfect to ramp-up new colleagues on the project** or to **help juniors to grow faster** by learning
from more experienced developers. This way they can see how you do things on your project and can also try out by 
themselves under your guidance and observation. Of course, the more experienced developer should pay attention all the time 
on how he shares his knowledge so that the pair programming doesn't become a mentorship instead.

By applying this practice, they will become more valuable to the team and to the company in a shorter time.






 


## Inline HTML elements

HTML defines a long list of available inline tags, a complete list of which can be found on the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

- **To bold text**, use `<strong>`.
- *To italicize text*, use `<em>`.
- Abbreviations, like <abbr title="HyperText Markup Langage">HTML</abbr> should use `<abbr>`, with an optional `title` attribute for the full phrase.
- Citations, like <cite>&mdash; Mark otto</cite>, should use `<cite>`.
- <del>Deleted</del> text should use `<del>` and <ins>inserted</ins> text should use `<ins>`.
- Superscript <sup>text</sup> uses `<sup>` and subscript <sub>text</sub> uses `<sub>`.

Most of these elements are styled by browsers with few modifications on our part.

### Code

Cum sociis natoque penatibus et magnis dis `code element` montes, nascetur ridiculus mus.

{% highlight js %}
// Example can be run directly in your JavaScript console

// Create a function that takes two arguments and returns the sum of those arguments
var adder = new Function("a", "b", "return a + b");

// Call the function
adder(2, 6);
// > 8
{% endhighlight %}

### Lists

1. Vestibulum id ligula porta felis euismod semper.
2. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
3. Maecenas sed diam eget risus varius blandit sit amet non magna.

<dl>
  <dt>HyperText Markup Language (HTML)</dt>
  <dd>The language used to describe and define the content of a Web page</dd>

  <dt>Cascading Style Sheets (CSS)</dt>
  <dd>Used to describe the appearance of Web content</dd>

  <dt>JavaScript (JS)</dt>
  <dd>The programming language used to build advanced Web sites and applications</dd>
</dl>