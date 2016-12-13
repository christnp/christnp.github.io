---
layout: page
title: projects
permalink: /projects/
description: landing page for all projects
---

{% for project in site.projects %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <p> Open Project <p>
            <h1>{{ project.title }}</h1>
            <br/>
            <br/>
            <br/>
            <p>{{ project.abstract }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ project.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <p> Open Project <p>
            <h1>{{ project.title }}</h1>
            <br/>
            <br/>
            <br/>
            <p>{{ project.abstract }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
