---
layout: page
title: "This is Marswoo "
description: "这里是我所有的文章 <br/> #也许就在哪天，你在自己的坚持下成为了一个巨人#"  
header-img: "images/semantic.jpg"  
---

{% for post in site.posts %}
{% if post.filtauthor == "marswoo" %}
<div class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
        <h2 class="post-title">
            {{ post.title }}
        </h2>
        {% if post.subtitle %}
        <h3 class="post-subtitle">
            {{ post.subtitle }}
        </h3>
        {% endif %}
        <div class="post-content-preview">
            {{ post.content | strip_html | truncate:150 }}
        </div>
    </a>
    <p class="post-meta">Posted by {% if post.author %}{{ post.author }}{% else %}{{ site.title }}{% endif %} on {{ post.date | date: "%B %-d, %Y" }}</p>
</div>

<hr>
{% endif %}
{% endfor %}
