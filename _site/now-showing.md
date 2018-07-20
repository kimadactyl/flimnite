{% for film in site.data.showings %}
  <h3>{{ film[0] }}</h3>
  <ul>
    {% for showing in film[1] %}
      <li>
        <strong>{{ showing.date }}, {{ showing.time }}</strong>.
        {{ showing.venue }}.
        Tickets: {{ showing.ticket }}.
        {% if showing.facebook %}
          <a href="{{ showing.facebook }}">Attend on Facebook</a>
        {% endif %}
        {% if showing.open_mic %}
          <a href="mailto:{{ showing.open_mic }}">Apply for the Open Mic</a>.
        {% endif %}
      </li>
    {% endfor %}
  </uL>
{% endfor %}
