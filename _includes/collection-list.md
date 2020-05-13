{% assign collections = site.collections | where: "state", "active" %}
<ul class="catalog">
    {% for collection in collections %}
    {% if collection.output != false %}
    <li><a href="/catalog/{{ collection.label }}"><span>{{ collection.name[site.active_lang] }}:</span> {{ collection.description[site.active_lang] }}</a></li>
    {% endif %}
    {% endfor %}
</ul>