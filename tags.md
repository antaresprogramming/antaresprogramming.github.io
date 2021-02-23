---
---
# Tags

<section class="tag-list">
{% assign tags = site.tags | sort %}
{% for tag in tags %}
  {% if tag[1].size > 1 %}
    {% assign id = tag[0] | replace: ' ', '-' %}
    <div class="latest" id="{{ id }}">
    <header class="flexify">
      <h2>#{{ tag[0] }}</h2>
    </header>
    {% assign posts = tag[1] | sort | reverse %}
    {% for post in posts %}
      {% unless post.hidden %}
        {% include post-card.html post=post %}
      {% endunless %}
    {% endfor %}
    </div>
  {% endif %}
{% endfor %}
</section>
