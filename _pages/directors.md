---
permalink: "/directors/"
layout: singlePage
title:  "Directors"
---

<section class="text-white" id="news" style="background-color:#1a5281">
      <div class="container">

{% assign rows = site.directors.size | divided_by: 3.0 | ceil %}
{% for i in (1..rows) %}

  <div class="row">

  {% assign offset = forloop.index0 | times: 3 %}
  {% for director in site.directors limit:3 offset:offset %}
 
  <div class="col-sm-4">
  <div class="card" style="height: 100%;">
  <div class="card-header"><strong>{{ director.name }}</strong> <p><em>{{ director.title }}</em> </p></div>
  <div class="card-body">
  <img class="pull-left" src="{{ director.photo }}" style="height:100px; width:100px; margin:10px" alt="Card image cap">
  <p class="card-text">{{ director.bio }}</p>
  </div>
  </div>
  </div>
  {% endfor %}

</div>

{% endfor %}

</div>
</section>

