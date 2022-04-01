---
layout: page
title: Publications
permalink: /publications/
---

<h3>Publications</h3>

{% for member in site.data.research %}

  <div>
    <a href="{{ member.pdf }}"><strong>{{ member.title }}</strong></a>.
    <p class="publication">{{ member.authors }}</p>
    <p class="publication"><i>{{ member.venue }}</i></p>
    <p class="publication">
    {% if member.slides %}
    [
    <a href="{{ member.slides }}">Talk slides</a>
    ]
    {% endif %}
    {% if member.blog %}
    [
    <a href="{{ member.blog }}">Blog post</a>
    ]
    {% endif %}
    {% if member.website %}
    [
    <a href="{{ member.website }}">Website</a>
    ]
    {% endif %}
    {% if member.corpus %}
    [
    <a href="{{ member.corpus }}">Corpus</a>
    ]
    {% endif %}
    {% if member.video %}
    [
    <a href="{{ member.video }}">Video</a>
    ]
    {% endif %}
    {% if member.code %}
    [
    <a href="{{ member.code }}">Code</a>
    ]
    {% endif %}
    {% if member.note %}
      {% if member.slides or member.blog or member.website or member.code %}
        <br />
      {% endif %}
    <span style="color:steelblue"><img src="/files/award.png" height="20" width="20" style="margin-right:5px; margin-top: 5px;"><img><strong>{{ member.note }}</strong></span>
    {% endif %}
    {% if member.comment %}
      {% if member.slides or member.blog or member.website or member.code or member.note %}
        <br />
      {% endif %}
    <span style="color:steelblue"><strong>{{ member.comment }}</strong></span>
    {% endif %}
    </p>
    <br />
  </div>
{% endfor %}

