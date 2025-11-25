<h1 id="publications"></h1>

<h2 style="margin: 60px 0px -15px;">
  Publications 
  <temp style="font-size:15px;">[</temp>
  <a href="https://scholar.google.com/citations?user=Qi2PSmEAAAAJ" target="_blank" style="font-size:15px;">Google Scholar</a>
  <temp style="font-size:15px;">]</temp>
  <temp style="font-size:15px;">[</temp>
  <a href="https://dblp.org/pid/12/10033-1.html" target="_blank" style="font-size:15px;">DBLP</a>
  <temp style="font-size:15px;">]</temp>
</h2>

<div class="publications">
<ol class="bibliography">


<!-- ===================== BOOKS ===================== -->
{% if site.data.publications.books %}
<h3 style="margin-top:40px;">Books</h3>
{% for link in site.data.publications.books %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative; padding-right: 15px; padding-left: 15px;">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width:100px; height:auto;">
    <abbr class="badge">Book</abbr>
  </div>

  <div class="col-sm-9" style="padding-right: 15px; padding-left: 20px;">
      <div class="title"><a href="{{ link.link }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.publisher }}</em></div>
  </div>
</div>
</li>

<br>
{% endfor %}
{% endif %}


<!-- ===================== BOOK CHAPTERS ===================== -->
{% if site.data.publications.chapters %}
<h3 style="margin-top:40px;">Book Chapters</h3>
{% for link in site.data.publications.chapters %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="padding-right: 15px; padding-left: 15px;">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width:100px; height:auto;">
    <abbr class="badge">Chapter</abbr>
  </div>

  <div class="col-sm-9" style="padding-right: 15px; padding-left: 20px;">
      <div class="title"><a href="{{ link.link }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.book }}</em></div>
  </div>
</div>
</li>

<br>
{% endfor %}
{% endif %}


<!-- ===================== JOURNAL ARTICLES ===================== -->
{% if site.data.publications.journals %}
<h3 style="margin-top:40px;">Journal Articles</h3>
{% for link in site.data.publications.journals %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="padding-right: 15px; padding-left: 15px;">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width:100px; height:auto;">
    <abbr class="badge">{{ link.short }}</abbr>
  </div>

  <div class="col-sm-9" style="padding-right: 15px; padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.journal }}</em></div>

      <div class="links">
        {% if link.pdf %}
        <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
        {% endif %}
      </div>
  </div>
</div>
</li>

<br>
{% endfor %}
{% endif %}


<!-- ===================== PREPRINTS ===================== -->
{% if site.data.publications.preprints %}
<h3 style="margin-top:40px;">Preprints</h3>
{% for link in site.data.publications.preprints %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="padding-right: 15px; padding-left: 15px;">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width:100px; height:auto;">
    <abbr class="badge">Preprint</abbr>
  </div>

  <div class="col-sm-9" style="padding-right: 15px; padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.venue }}</em></div>

      <div class="links">
        {% if link.pdf %}
        <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
        {% endif %}
      </div>
  </div>
</div>
</li>

<br>
{% endfor %}
{% endif %}


<!-- ===================== CONFERENCES ===================== -->
{% if site.data.publications.conferences %}
<h3 style="margin-top:40px;">Conference Papers</h3>
{% for link in site.data.publications.conferences %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="padding-right: 15px; padding-left: 15px;">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width:100px; height:auto;">
    <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>

  <div class="col-sm-9" style="padding-right: 15px; padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>

      <div class="links">
        {% if link.pdf %}
        <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
        {% endif %}

        {% if link.page %}
        <a href="{{ link.page }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">Project Page</a>
        {% endif %}

        {% if link.code %}
        <a href="{{ link.code }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">Code</a>
        {% endif %}

        {% if link.bibtex %}
        <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">BibTex</a>
        {% endif %}

        {% if link.notes %}
        <strong><i style="color:#e74d3c; font-weight:600">{{ link.notes }}</i></strong>
        {% endif %}
      </div>

  </div>
</div>
</li>

<br>
{% endfor %}
{% endif %}


</ol>
</div>
