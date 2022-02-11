---
layout: page
permalink: /snippets/
title: Code snippets
---

<nav>
	<a href="{{ site.baseurl }}/searchSnippets">Search</a>
</nav><br>

<div id="archives">
{% for page in site.pages %}
    {% if page.snippet %}
        <article class="post">
              <a href="{{ site.baseurl }}{{ page.url }}">
                <h1>{{ page.title }}</h1>
                <div>
                    <p class="post_date">{{ page.date | date: "%B %e, %Y" }}</p>
                </div>
              </a>
              <div class="entry">
                {{ page.excerpt }}
              </div>
        
              <a href="{{ site.baseurl }}{{ page.url }}" class="read-more">Read More</a>
        </article>
    {% endif %}
{% endfor %}
</div>