<h1>Now Showing</h1>

<p>Here's our listings, clickety click</p>

{% for film in site.data.showings %}
  <h2>{{ film[0] }}</h2>
  <ul class="showings">
    {% for showing in film[1] %}
      <li class="showing">
        <div class="showing__content">
          <div class="showing__date">
            <h3>{{ showing.date | date: '%A %-d %B' }}, {{ showing.time }}</h3>
          </div>
          <div class="showing__venue">
            {{ showing.venue }}
          </div>
          <div class="showing__tickets">
            Tickets: {{ showing.ticket }}
          </div>
          <div class="showing__facebook">
            {% if showing.facebook %}
              <a href="{{ showing.facebook }}">Attend on Facebook</a>
            {% endif %}
          </div>
          <div class="showing__openmic">
            {% if showing.open_mic %}
              <a href="mailto:{{ showing.open_mic }}?subject=I'd like to perform at {{ film[0] }} on {{ showing.date }}!">Apply for the Open Mic</a>
            {% endif %}
          </div>
        </div>
        <div class="showing__image">
          <img src="https://placedog.net/400/400" alt="Poster for {{ flim[0] }}">
        </div>
      </li>
    {% endfor %}
  </ul>
{% endfor %}
