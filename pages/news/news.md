---
title: News
sidebar: home_sidebar
keywords: news, blog, updates, release notes, announcements
permalink: news.html
toc: false
folder: news
---

<div class="home">

    <div class="post-list">
        {% for post in site.posts limit:10 %}


    <h2><a class="post-link" href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }} /
            {% for tag in post.tags %}
                <a href="{{ site.baseurl }}{{ "/tag_" | append: {{tag}}.html">{{tag}}</a>{% unless forloop.last %}, {% endunless%}
                {% endfor %}</span>
        <p>{% if page.summary %} {{ page.summary | strip_html | strip_newlines | truncate: 160 }} {% else %} {{ post.content | truncatewords: 50 | strip_html }} {% endif %}</p>



        {% endfor %}

        <p><a href="{{ "/feed.xml" | prepend: site.baseurl }}" class="btn btn-primary navbar-btn cursorNorm" role="button">RSS Subscribe{{tag}}</a></p>

<hr />
        <p>See more posts from the <a href="{{ "/news_archive.html" | prepend: site.baseurl }}">News Archive</a>. </p>


</div>