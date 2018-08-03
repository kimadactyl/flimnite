# Crew

## History of Flim

## The Team

### Jasmine

### Jack

## Collaborators

<ul class="showings">
  {% for crew in site.data.crew %}
    <li class="showing">
      <div class="showing__content">
        <h3>{{ crew.name }}</h3>
        {{ crew.bio | markdown }}
      </div>
      <div class="showing__image">
        <img src="{{ crew.image }}" alt="An image of {{ crew.name }}">
      </div>
    </li>
  {% endfor %}
</ul>
