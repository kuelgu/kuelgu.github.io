---
layout: layout
title: kuelgu's github
---
# now printing

<ul>
{% for post in site.posts %}
  <li>
    <a href="{{ post.url }}">{{ post.date | date_to_long_string }} : {{ post.title }}</a>
  </li>
{% endfor %}
</ul>


**Copyright © {{ site.author.name }} 2012 All rights reserved. Please contact to {{ site.author.email }}.**
