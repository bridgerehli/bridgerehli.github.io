<h2 id="publications" style="margin: 2px 0px 10px;">Publications</h2>

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
  <em>{{ link.conference }}</em>
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
  <em>{{ link.conference }}</em>
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
  <strong>{{ link.title }}</strong><br>
{% if link.authors and link.authors != "" %}
{{ link.authors }}<br>
{% endif %}
  <em>{{ link.conference }}</em>
</div>
{% endif %}
{% endfor %}
</div>

</div>
