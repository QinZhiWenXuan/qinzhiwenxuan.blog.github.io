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
<h2 class="post-list-heading">Posts</h2>
<ul class="post-list">
<li><span class="post-meta">Aug 6, 2018</span>
        <h3>
          <a class="post-link" href="/formal/java/2018/08/06/slf4j.html">
            slf4j-logback
          </a>
        </h3></li>
</ul>
<p class="rss-subscribe">subscribe <a href="/feed.xml">via RSS</a></p>
<script>
  window.onload = function () {
        try {
            var postHead = document.getElementsByClassName("post-list-heading");
            var postList = document.getElementsByClassName("post-list");
            var subscribe = document.getElementsByClassName("rss-subscribe");
            console.debug(postHead);
            console.debug(postList);
            console.debug(subscribe);
            for (var i = 0; i < postHead.length ; i++) {
                var t = postHead[i] ;
                t.parentNode.removeChild(t);
            }
            for (var i = 0; i < postList.length ; i++) {
               var t = postList[i] ;
               t.parentNode.removeChild(t);
            }
            for (var i = 0; i < subscribe.length ; i++) {
               var t = subscribe[i] ;
               t.parentNode.removeChild(t);
            }

        }catch (e) {
            console.error(e);
        }
  }
</script>