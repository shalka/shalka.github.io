---
layout: page
title: so-blog
tagline: all the things i do instead of sleeping
---
{% include JB/setup %}

<div class="posts-heading">Posts</div>
(to see more than the last 10 posts, check out the archive)

<div class="posts-listing">
  {% for post in site.posts limit:10 %}
    <p>
      <h3><a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
      <span class="post-meta">
        <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
        <span class="post-meta-spacer"> | </span>
        <span class="post-excerpt">{{ post.description | remove: '<p>' | remove: '</p>' }}</span>
        <span class="post-meta-spacer"> | </span>
        <span>{% for tag in post.tags %}#{{ tag }} {% endfor %}</span>
      </span>
    </p>
  {% endfor %}
</div>
