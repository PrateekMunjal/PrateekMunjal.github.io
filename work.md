---
layout: page
title: Interests
permalink: /work/
---




### Following enlist all the posts written so far:
<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>

### Contact me

[2017CSM1009@iitrpr.ac.in](mailto:2017CSM1009@iitrpr.ac.in)
[prateekmunjal31@google.com](mailto:prateekmunjal31@google.com)