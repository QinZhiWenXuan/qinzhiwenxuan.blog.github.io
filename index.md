---
---
<ul class="list pa0">
  {% for post in site.posts %}
      {% for categorie in post.categories %}
          {% if categorie == 'formal' %}
              <li class="mv2">
                  <a href="{{ site.url }}{{ post.url }}" class="db pv1 link blue hover-mid-gray">
                    <time class="fr silver ttu">
                        {{ post.date | date: "%Y-%m-%d"  }}
                    </time>
                        {{ post.title }}
                  </a>
               </li>
          {% endif %}
      {% endfor %}
  {% endfor %}
</ul>
