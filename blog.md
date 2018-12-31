---
layout: page
title: Machine Learning Research
permalink: /blog/
---
Hi reader! I will be sharing my posts here, which will be focused on different papers and implementation hacks in the area of machine learning research. If you find any mistake, please feel free to comment under the comment section of related post. Alternatively, one can also write up to my email, i.e, 2017csm1009@iitrpr.ac.in -- Just remember to add a subject line: **'_regardind blog <blog\_title>_'**

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