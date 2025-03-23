---
title:
layout: default
permalink: /gifts/
published: true
---


<div class="giftContainer">

	<div class="gallery">


  {% for gift in site.gifts %}

  {% if gift.redirect %}
  <div class="giftTile">
          <a href="{{ gift.redirect }}" target="_blank">
          <span>
              <h2>{{ gift.title }}</h2>
              <br/>
              <p>{{ gift.description }}</p>
          </span>
          </a>
  </div>

  {% else %}

  <div class="giftTile">
          <a href="{{ gift.url | prepend: site.baseurl | prepend: site.url }}">
          <span>
              <h2>{{ gift.title }}</h2>
              <br/>
              <p>{{ gift.description }}</p>
          </span>
          </a>
  </div>

  {% endif %}

  {% endfor %}

	</div>

</div>
