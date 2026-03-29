
<div class="publications">

<!-- BOOKS -->
<h3>Books</h3>
<div class="bibliography">
{% for link in site.data.publications.main %}
{% if link.type == "book" %}
<div style="margin-bottom: 1.2em;">
  <strong>{{ link.title }}</strong><br>
 {% if link.authors and link.authors != "" %}
{{ link.authors }}<br>
{% endif %}
  {% if link.type == "article" %}   <em>{{ link.conference }}</em>{% if link.year %}, {{ link.year }}{% endif %} {% elsif link.type == "book" %}   {{ link.conference }}{% if link.year %}, {{ link.year }}{% endif %} {% else %}   <em>{{ link.conference }}</em>{% if link.year %}, {{ link.year }}{% endif %} {% endif %}
</div>
{% endif %}
{% endfor %}
</div>

<!-- ARTICLES -->
<h3>Articles</h3>
<div class="bibliography">
{% for link in site.data.publications.main %}
{% if link.type == "article" %}
<div style="margin-bottom: 1.2em;">
  {% if link.pdf %}
    <a href="{{ link.pdf }}"><strong>{{ link.title }}</strong></a>
  {% else %}
    <strong>{{ link.title }}</strong>
  {% endif %}<br>
{% if link.authors and link.authors != "" %}
{{ link.authors }}<br>
{% endif %}
  {% if link.type == "article" %}   <em>{{ link.conference }}</em>{% if link.year %}, {{ link.year }}{% endif %} {% elsif link.type == "book" %}   {{ link.conference }}{% if link.year %}, {{ link.year }}{% endif %} {% else %}   <em>{{ link.conference }}</em>{% if link.year %}, {{ link.year }}{% endif %} {% endif %}
</div>
{% endif %}
{% endfor %}
</div>

<!-- REVIEWS -->
<h3>Reviews</h3>
<div class="bibliography">
{% for link in site.data.publications.main %}
{% if link.type == "review" %}
<div style="margin-bottom: 1.2em;">
  {% if link.link %}
  <a href="{{ link.link }}"><strong>{{ link.title }}</strong></a><br>
{% elsif link.pdf %}
  <a href="{{ link.pdf }}"><strong>{{ link.title }}</strong></a><br>
{% else %}
  <strong>{{ link.title }}</strong><br>
{% endif %}
{% if link.authors and link.authors != "" %}
{{ link.authors }}<br>
{% endif %}
  {% if link.type == "article" %}   <em>{{ link.conference }}</em>{% if link.year %}, {{ link.year }}{% endif %} {% elsif link.type == "book" %}   {{ link.conference }}{% if link.year %}, {{ link.year }}{% endif %} {% else %}   <em>{{ link.conference }}</em>{% if link.year %}, {{ link.year }}{% endif %} {% endif %}
</div>
{% endif %}
{% endfor %}
</div>

</div>
