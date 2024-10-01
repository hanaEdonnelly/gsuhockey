---
layout: page
title: News
pagination:
  enabled: true
description: Stay updated with the latest news and updates from the South Carolina Gamecocks women's rugby team.
---


<div id="posts">
    {% for post in site.posts %}
        <div class="post-teaser">
            {% if post.thumbnail %}
            <div class="post-img">
                <a aria-label="{{ post.title }}" href="{{ post.url | relative_url }}">
                    <img alt="{{ post.title }}" src="{{ post.thumbnail | relative_url }}">
                </a>
                <span>
            <header>
                <h2>
                <a aria-label="{{ post.title }}" class="post-link" href="{{ post.url | relative_url }}">
                    {{ post.title }}
                </a>
                </h1>
                {% include blog/post_info.liquid author=post.author date=post.date %}
            </header>
            {% if site.excerpt or site.theme_settings.excerpt %}
                <div class="excerpt">
                    {% if site.excerpt == "truncate" %}
                        {{ post.content | strip_html | truncate: '250' | escape }}
                    {% else %}
                        {{ post.excerpt | strip_html | escape }}
                    {% endif %}
                </div>
            {% endif %}
            </span>
            </div>
            {% endif %}

        <div class="post-teaser">
            <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
          <p><em>{{ post.date | date: "%B %d, %Y" }}</em></p>
            <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
        </div>
    {% endfor %}
</div>
<div class="pagination">
    {% if site.previous_page %}
        <a class="previous" href="{{ site.previous_page_path | relative_url }}">Previous</a>
    {% endif %}

    {% if site.next_page %}
        <a class="next" href="{{ site.next_page_path | relative_url }}">Next</a>
    {% endif %}
</div>
