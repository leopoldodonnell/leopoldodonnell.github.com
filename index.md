---
layout: page
title: 
tagline:
---
{% include JB/setup %}
  
<h2>Just RTFM</h2>

If it were really only about the programming. This blog and blather is my collection of things I've learnt
and/or shared via [Leo's github](https://github.com/leopoldodonnell). [more...]({% post_url 2013-03-24-just-rtfm %}) 

---

<!-- using the split filter -->
{% for post in site.posts limit:10 %}
   <div class="post-preview row">
   <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
   <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
   {{ post.content | split:'<!--break-->' | first }}
   {% if post.content contains '<!--break-->' %}
      <a href="{{ post.url }}">read more</a>
   {% endif %}
   </div>
   <hr class="clearfix">
{% endfor %}

---

