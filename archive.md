---
layout: page
title: Archive
permalink: /archive/
---

<ul class="post-list">
    {% for post in site.posts %}
      <li>
        <header class="post-header">
          <h1 class="post-title" itemprop="name headline">
            <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          </h1>
          <p class="post-meta"><time datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">{{ post.date | date: "%b %-d, %Y" }}</time>{% if post.author %} • <span itemprop="author" itemscope itemtype="http://schema.org/Person"><span itemprop="name">{{ post.author }}</span></span>{% endif %}</p>
        </header>
          {{ post.excerpt }}
        <hr/>
      </li>
    {% endfor %}
  </ul>
