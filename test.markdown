---
layout: null
---
<h1>Test 2</h1>
{% assign collections = site.collections | where:"label", "categories" %}

{% for collection in collections %}
{% unless collection.label == 'posts' %}
<h2>{{collection.label}}</h2>
<ul>
    {% for file in collection.files %}
    <li><a href="{{ file.path | remove: "_" }}">{{ file.path | remove: "_" }}</a></li>
    {% endfor %}
</ul>
{% endunless %}
{% endfor %}