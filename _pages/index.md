---
layout: default
permalink: /
---

My name is Hao Tran, and this is where I attempt to document my lifestyle and technological experiments—whether they are successful endeavours or complete failures. Other times, I write about my thoughts on various topics, or observations on everyday life.

Most of these posts were written for selfish reasons—wanting to vaguely keep track of what I was thinking about and working on that I can refer back to in the future. Some posts are living documents.

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
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <span class="list-date">{{ post.date | date: "%b %d" }}</span>
      </li>
    </ul>

  </section>
{% endfor %}
