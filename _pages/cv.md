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
            <h3>{{ page.position }}</h3>
            <div>
                <p class="post_date">{{ page.title }} <br>{{ page.start }} - {{ page.end }}</p>
            </div>
        </article>
    {% endif %}
{% endfor %}
</div>