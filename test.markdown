---
layout: null
---

{% for collection in site.collections | where:"label", "categories" %}
{% unless collection.label == 'posts' %}
<h2>{{collection.label}}</h2>
<ul>
    {% for file in collection.files %}
    <li><a href="{{ file.path | remove: "_" }}">{{ file.path | remove: "_" }}</a></li>
    {% endfor %}
</ul>
{% endunless %}
{% endfor %}