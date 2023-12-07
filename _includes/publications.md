<h2 id="research-papers" style="margin: 2px 0px -15px;">Research Papers</h2>

<div class="publications">
  <ol class="bibliography">

    {% for link in site.data.publications.main %}

    <li style="margin-bottom: 10px;"> <!-- Adjust the margin-bottom to control the gap between papers -->
      <div class="pub-row" style="display: flex; align-items: flex-start;"> <!-- align-items: flex-start ensures top alignment -->
        <div class="col-sm-3 abbr" style="position: relative; padding-right: 5px; padding-left: 5px;">
          {% if link.image %} 
            <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="max-width: 90%; height: auto;">
          {% endif %}
          {% if link.conference_short %} 
            <abbr class="badge">{{ link.conference_short }}</abbr>
          {% endif %}
        </div>
        <div class="col-sm-9" style="position: relative; padding-right: 10px; padding-left: 10px;">
          <div>
            <div class="title"><strong>{{ link.title }}</strong></div>
            <div class="author">{{ link.authors }}</div>
            <div class="periodical"><em>{{ link.conference }}</em></div>
            <div class="links">
              {% if link.pdf %} 
                <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
              {% endif %}
              {% if link.code %} 
                <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
              {% endif %}
              {% if link.page %} 
                <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
              {% endif %}
              {% if link.bibtex %} 
                <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
              {% endif %}
              {% if link.notes %} 
                <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
              {% endif %}
              {% if link.others %} 
                {{ link.others }}
              {% endif %}
            </div>
          </div>
        </div>
      </div>
    </li>

    {% endfor %}

  </ol>
</div>
