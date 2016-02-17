---
layout: null
---
<h1>Test 4</h1>
{% assign collections = site.collections | where:"label", "categories" %}

{% for collection in collections %}
<h2>{{collection}}</h2>
<h2>{{collection.label}}</h2>
<ul>
    {% for doc in collection.docs %}
    <li><a href="{{ doc.path | remove: "_" }}">{{ doc.path | remove: "_" }}</a></li>
    {% endfor %}
</ul>
{% endfor %}


{% assign collections = site.categories %}

<h2>Category List</h2>
<ul>
{% for collection in collections %}
<li>{{collection}}</li>
{% endfor %}
</ul>
