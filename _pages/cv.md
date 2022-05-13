---
layout: post
permalink: /cv/
title: Curriculum Vitae
---

## Work Experience

<div id="archives">
{% assign work_exps = site.pages | where: "type", "work" %}
{% for page in work_exps reversed %}
    <article class="post">
        <h3>{{ page.position }}</h3>
        <div>
            <p class="author_title">{{ page.title }} <br>{{ page.start }} - {{ page.end }}</p>
        </div>
        <div class="entry">
            {{ page.content }}
        </div>{% if page.tech_stack %}
        <div>Tech stack: </div>{% for tech in page.tech_stack %}<div class="tech-tag">{{tech}}</div>{% unless forloop.last %}&nbsp;{% endunless %}{% endfor %}{% endif %}     
    </article>
{% endfor %}
</div>

## Education

<div id="archives">
{% assign educations = site.pages | where: "type", "education" %}
{% for page in educations reversed %}
    <article class="post">
        <h3>{{ page.position }}</h3>
        <div>
            <p class="author_title">{{ page.institution }} <br>{{ page.start }} - {{ page.end }}</p>
        </div>
        <div class="entry">
            {{ page.content }}
        </div>
    </article>
{% endfor %}
</div>


