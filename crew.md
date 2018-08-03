# Crew

## Your Hosts

<div class="hosts">
  <div class="host">
    <h3>Jasmine</h3>
    <img src="https://placedog.net/400/400" alt="A photo of Jasmine">
    <p>Jasmine Chatfield is the co-host and producer of FLIM NITE. Jasmine is also a writer, theatre-maker and comedian. They co-created comedy sci-fi show ‘Clonely’ as one half of Me Me Me and took it to the Edinburgh Fringe and on tour throughout 2017 and 2018. In 2017 they received a Northern Writers Award as part of the New North Poets group. Jasmine’s special skill is getting booed by audiences.</p>
  </div>
  <div class="host">
    <h3>Jack</h3>
    <img src="https://placedog.net/400/400" alt="A photo of Jack">
    <p>Jack Nicholls is the co-host and artistic director of FLIM NITE. He makes comedy with the sketch group Beach Hunks. His first poetry pamphlet, ‘Meat Songs’, was released by The Emma Press in 2017. His fiction and poetry have been published in The Poetry Review, The Best New British and Irish Poets 2017, PANK, and other places. Jack’s special skill is putting his hand on his hip and looking mischievous.</p>
  </div>
</div>

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
