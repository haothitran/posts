---
layout: default
permalink: /
--- 

My name is Hao Tran, and this is where I document my lifestyle and technological experiments. Other times, I write about my thoughts on various topics of personal interest or observations of everyday life. Some posts are living documents.

{% for post in site.posts %}
  <section>

    {% unless post.next %}
      <h2 class="list-year">{{ post.date | date: '%Y' }}</h2>
    {% else %}
      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
      {% if year != nyear %}
        <h2 class="list-year">{{ post.date | date: '%Y' }}</h2>
      {% endif %}
    {% endunless %}

    <ul class="list-posts">
      <li>
          <span class="list-date">{{ post.date | date: "%m.%d" }}</span>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </li>
    </ul>

  </section>
{% endfor %}
