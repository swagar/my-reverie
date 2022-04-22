---
layout: post
permalink: /cv/
title: Curriculum Vitae
---

## Work Experience

<div id="archives">
{% for page in site.pages reversed %}
    {% if page.type == "work" %}
        <article class="post">
            <h3>{{ page.position }}</h3>
            <div>
                <p class="author_title">{{ page.title }} <br>{{ page.start }} - {{ page.end }}</p>
            </div>
            <div class="entry">
                {{ page.content }}
            </div> 
        </article>
    {% endif %}
{% endfor %}
</div>