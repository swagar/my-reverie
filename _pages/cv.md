---
layout: page
permalink: /cv/
title: Curriculum Vitae
---
## Work Experience

<div id="archives">
{% for page in site.pages %}
    {% if page.type == "work" %}
        <article class="post">
            <h1>{{ page.title }}</h1>
            ## {{ page.title }}
            <div>
                <p class="post_date">{{ page.position }}</p>
            </div>
            <div class="entry">
                {{ page.excerpt }}
            </div>
        </article>
    {% endif %}
{% endfor %}
</div>