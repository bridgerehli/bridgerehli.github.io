<h2 id="publications" style="margin: 2px 0px 10px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li style="margin-bottom: 1.2em;">

  <div class="title">
    {% if link.pdf %}
      <a href="{{ link.pdf }}"><strong>{{ link.title }}</strong></a>
    {% else %}
      <strong>{{ link.title }}</strong>
    {% endif %}
  </div>

  <div class="author">
    {{ link.authors }}
  </div>

  <div class="periodical">
    <em>{{ link.conference }}</em>
  </div>

  <div class="links" style="font-size: 0.9em;">
    {% if link.pdf %} 
      <a href="{{ link.pdf }}" target="_blank">PDF</a>
    {% endif %}
    {% if link.code %} 
      | <a href="{{ link.code }}" target="_blank">Code</a>
    {% endif %}
    {% if link.page %} 
      | <a href="{{ link.page }}" target="_blank">Page</a>
    {% endif %}
    {% if link.bibtex %} 
      | <a href="{{ link.bibtex }}" target="_blank">Bib</a>
    {% endif %}
  </div>

</li>

{% endfor %}

</ol>
</div>
