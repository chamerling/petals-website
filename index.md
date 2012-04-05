---
layout: page
title: Home
tagline: Petals Community
---
{% include JB/setup %}

<div class="row">
    <div class="span6 offset1">
        <div class="hero-unit">
            <h1>Welcome!</h1>
            <p>Soon, you'll find here a set of documentations dedicated to Petals Community.</p>
        </div>
    </div>
    <div class="span4 offset1">
        <div class="well">
            <h2>Last posts</h2>
            <ul>
                {% for post in site.posts %}
                <li><span>{{ post.date | date: "%B %e, %Y" }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{post.title }}</a><br/>
                    {% for tag in post.tags %}&nbsp;<span class="label label-{{ tag }}">{{ tag }}</span>{% endfor %}
                </li>
                {% endfor %}
            </ul>
        </div>
    </div>
</div>

