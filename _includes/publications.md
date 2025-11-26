<h1 id="publications"></h1>

<h2 style="margin: 60px 0px 25px;">   <!-- Increased bottom margin from -15px to 25px -->
  Publications
  <temp style="font-size:15px;">[</temp>
  <a href="https://scholar.google.com/citations?user=KQUQlG4AAAAJ&hl=en" target="_blank" style="font-size:15px;">Google Scholar</a>
  <temp style="font-size:15px;">]</temp>
</h2>

<style>
.pub-img {
  width: 100%;
  max-width: 180px;
  height: 120px;
  object-fit: cover;
  border-radius: 8px;
  border: 1px solid #ddd;
}

.badge {
  position: absolute;
  top: 5px;         /* moved from bottom to top */
  left: 10px;
  background: #444;
  color: white;
  padding: 2px 6px;
  font-size: 11px;
  border-radius: 4px;
}

.pub-row {
  display: flex;
  flex-wrap: wrap;
}

.pub-left {
  width: 180px;
  padding: 10px;
  position: relative;
}

.pub-right {
  flex: 1;
  padding: 10px 20px;
}

.pub-title {
  font-weight: bold;
  font-size: 17px;
}

/* Extra spacing between categories */
h3 {
  margin-top: 40px;   /* increased spacing before section titles */
  margin-bottom: 10px;
}
</style>


<div class="publications">
<ol class="bibliography">


<!-- ============ BOOKS ============ -->
{% if site.data.publications.books %}
<h3>Books</h3>
{% for link in site.data.publications.books %}
<li>
<div class="pub-row">

  <div class="pub-left">
    <img src="{{ link.image }}" class="pub-img">
    <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>

  <div class="pub-right">
    <div class="pub-title">
      <a href="{{ link.pdf | default: link.page }}">{{ link.title }}</a>
    </div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>

    <div class="links">
      {% if link.pdf %}
      <a href="{{ link.pdf }}" target="_blank"
        class="btn btn-sm z-depth-0" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.page %}
      <a href="{{ link.page }}" target="_blank"
        class="btn btn-sm z-depth-0" style="font-size:12px;">Page</a>
      {% endif %}
    </div>
  </div>

</div>
</li>
<br>
{% endfor %}
{% endif %}


<!-- ============ BOOK CHAPTERS ============ -->
{% if site.data.publications.book_chapters %}
<h3>Book Chapters</h3>
{% for link in site.data.publications.book_chapters %}
<li>
<div class="pub-row">

  <div class="pub-left">
    <img src="{{ link.image }}" class="pub-img">
    <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>

  <div class="pub-right">
    <div class="pub-title">
      <a href="{{ link.pdf | default: link.page }}">{{ link.title }}</a>
    </div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>
  </div>

</div>
</li>
<br>
{% endfor %}
{% endif %}


<!-- ============ JOURNALS ============ -->
{% if site.data.publications.journals %}
<h3>Journal Articles</h3>
{% for link in site.data.publications.journals %}
<li>
<div class="pub-row">

  <div class="pub-left">
    <img src="{{ link.image }}" class="pub-img">
    <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>

  <div class="pub-right">
    <div class="pub-title">
      <a href="{{ link.pdf }}">{{ link.title }}</a>
    </div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>
  </div>

</div>
</li>
<br>
{% endfor %}
{% endif %}


<!-- ============ PREPRINTS ============ -->
{% if site.data.publications.preprints %}
<h3>Preprints</h3>
{% for link in site.data.publications.preprints %}
<li>
<div class="pub-row">

  <div class="pub-left">
    <img src="{{ link.image }}" class="pub-img">
    <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>

  <div class="pub-right">
    <div class="pub-title">
      <a href="{{ link.pdf }}">{{ link.title }}</a>
    </div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>
  </div>

</div>
</li>
<br>
{% endfor %}
{% endif %}


<!-- ============ CONFERENCES ============ -->
{% if site.data.publications.conferences %}
<h3>Conference Papers</h3>
{% for link in site.data.publications.conferences %}
<li>
<div class="pub-row">

  <div class="pub-left">
    <img src="{{ link.image }}" class="pub-img">
    <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>

  <div class="pub-right">
    <div class="pub-title">
      <a href="{{ link.pdf }}">{{ link.title }}</a>
    </div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>

    {% if link.notes %}
    <strong style="color:#e74d3c;">{{ link.notes }}</strong>
    {% endif %}
    {% if link.notes2 %}
    <strong style="color:#e74d3c;">{{ link.notes2 }}</strong>
    {% endif %}
  </div>

</div>
</li>
<br>
{% endfor %}
{% endif %}

</ol>
</div>
