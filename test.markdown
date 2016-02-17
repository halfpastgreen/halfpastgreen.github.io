---
layout: null
---
<h1>Test 3</h1>
{% assign collections = site.collections | where:"label", "categories" %}

{% for collection in collections %}
<h2>{{collection}}</h2>
<h2>{{collection.label}}</h2>
<ul>
    {% for file in collection.files %}
    <li><a href="{{ file.path | remove: "_" }}">{{ file.path | remove: "_" }}</a></li>
    {% endfor %}
</ul>
{% endfor %}