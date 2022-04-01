---
layout: page
title: Press
permalink: /press/
---

<h3>Press</h3>

{% for member in site.data.press %}

  <div>
    <a href="{{ member.url }}"><strong>{{ member.title }}</strong></a>.
    <p class="publication">{{ member.venue }}</p>
    <p class="publication">{{ member.date }}</p>
    <br/>
  </div>

{% endfor %}

