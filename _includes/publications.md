<h2 id="publications" style="margin: 2px 0px 10px;">Publications</h2>

<div class="publications">

<!-- BOOKS -->
<h3>Books</h3>
<ol class="bibliography">
{% for link in site.data.publications.main %}
{% if link.type == "book" %}
<li style="margin-bottom: 1.2em;">
  <strong>{{ link.title }}</strong><br>
  {{ link.authors }}<br>
  <em>{{ link.conference }}</em>
</li>
{% endif %}
{% endfor %}
</ol>

<!-- ARTICLES -->
<h3>Articles</h3>
<ol class="bibliography">
{% for link in site.data.publications.main %}
{% if link.type == "article" %}
<li style="margin-bottom: 1.2em;">
  {% if link.pdf %}
    <a href="{{ link.pdf }}"><strong>{{ link.title }}</strong></a>
  {% else %}
    <strong>{{ link.title }}</strong>
  {% endif %}<br>
  {{ link.authors }}<br>
  <em>{{ link.conference }}</em>
</li>
{% endif %}
{% endfor %}
</ol>

<!-- REVIEWS -->
<h3>Reviews</h3>
<ol class="bibliography">
{% for link in site.data.publications.main %}
{% if link.type == "review" %}
<li style="margin-bottom: 1.2em;">
  <strong>{{ link.title }}</strong><br>
  {{ link.authors }}<br>
  <em>{{ link.conference }}</em>
</li>
{% endif %}
{% endfor %}
</ol>

</div>
