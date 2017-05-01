---
layout: page
title: Anil Bhskar's Blog!
tagline: a computer science blog
---
{% include JB/setup %}

## Connect
<ul>
	<li><a href="https://www.linkedin.com/in/anil-bhaskar-08944a59/">LinkedIn</a></li>
	<li><a href="http://stackoverflow.com/users/1327585/anil-bhaskar">StackOverflow</a></li>
	<li><a href="https://www.hackerearth.com/@anilbhaskar.cse">Hackerearth</a></li>
</ul>   
## Posts


<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>



