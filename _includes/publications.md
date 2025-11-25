<h1 id="publications"></h1>

<h2 style="margin: 60px 0px -15px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

<!-- =======================
      BOOKS
     ======================= -->
<h3 style="margin-top: 40px;">Books</h3>
{% for link in site.data.publications.books %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1">
    <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>
  <div class="col-sm-9">
    <div class="title"><a href="{{ link.page }}">{{ link.title }}</a></div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>
  </div>
</div>
</li>
<br>
{% endfor %}

<!-- =======================
      BOOK CHAPTERS
     ======================= -->
<h3 style="margin-top: 40px;">Book Chapters</h3>
{% for link in site.data.publications.book_chapters %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1">
    <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>
  <div class="col-sm-9">
    <div class="title"><a href="{{ link.page }}">{{ link.title }}</a></div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>
  </div>
</div>
</li>
<br>
{% endfor %}

<!-- =======================
      JOURNAL ARTICLES
     ======================= -->
<h3 style="margin-top: 40px;">Journal Articles</h3>
{% for link in site.data.publications.journals %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1">
    <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>
  <div class="col-sm-9">
    <div class="title">
      {% if link.pdf %}
        <a href="{{ link.pdf }}">{{ link.title }}</a>
      {% else %}
        {{ link.title }}
      {% endif %}
    </div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>
  </div>
</div>
</li>
<br>
{% endfor %}

<!-- =======================
      PREPRINTS
     ======================= -->
<h3 style="margin-top: 40px;">Preprints</h3>
{% for link in site.data.publications.preprints %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1">
    <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>
  <div class="col-sm-9">
    <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>
    {% if link.notes %}
    <strong><i style="color:#e74d3c;">{{ link.notes }}</i></strong>
    {% endif %}
  </div>
</div>
</li>
<br>
{% endfor %}

<!-- =======================
      CONFERENCE PAPERS
     ======================= -->
<h3 style="margin-top: 40px;">Conference Papers</h3>
{% for link in site.data.publications.conferences %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1">
    <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>
  <div class="col-sm-9">
    <div class="title">
      {% if link.pdf %}
        <a href="{{ link.pdf }}">{{ link.title }}</a>
      {% else %}
        {{ link.title }}
      {% endif %}
    </div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>
    {% if link.notes %}
      <strong><i style="color:#e74d3c;">{{ link.notes }}</i></strong>
    {% endif %}
    {% if link.notes2 %}
      <strong><i style="color:#e74d3c;">{{ link.notes2 }}</i></strong>
    {% endif %}
  </div>
</div>
</li>
<br>
{% endfor %}

</ol>
</div>
