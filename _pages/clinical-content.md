---
permalink: "/clinical-content/"
layout: singlePage
title: "Clinical Content"
---
  <header class="lg masthead text-center text-white d-flex">
      <div class="container my-auto">
        <div class="row">
          <div class="col-lg-10 mx-auto">
            <h1 class="text-uppercase text-dark">
              <strong>{{ page.title }}</strong>
            </h1>
            <hr>
          </div>
          <div class="col-lg-8 mx-auto">
            <p class="text-faded text-dark mb-5">Introduction to clinical content subcommittee</p>
          </div>
        </div>
      </div>
    </header>

<section id="about" style="background-image:url(../img/blog-bg.png);background-position:center center;-webkit-background-size:cover;-moz-background-size:cover;-o-background-size:cover;background-size:cover">
      <div class="container">
        <div class="row">
          <div class="col-lg12 mx-auto text-center">
            <h1 class="text-uppercase text-dark">
              <strong>Subcommittee</strong>
            </h1>
            <h2 class="section-heading text-white">Our Subcommittee Members</h2>
            <hr class="light my-4">
                {% assign rows = site.subcommittee-members.size | divided_by: 3.0 | ceil %}
                {% for i in (1..rows) %}
                <div class="row">
                    {% assign offset = forloop.index0 | times: 3 %}
			{% assign sorted = site.subcommittee-members | sort:"role" %}
                       {% for subcommittee-member in sorted offset:offset limit:3 | sort: 'role' %} 
                        {% if subcommittee-member.subcommittee == page.title %}
                            <div class="col-sm-4">
                                <div class="card" style="height: 100%;">
                                    <div class="card-header"><strong>{{ subcommittee-member.name }}</strong> <p><em>{{ subcommittee-member.role }}</em> </p></div>
                                    <div class="card-body">
                                        <img class="pull-left" src="{{ subcommittee-member.photo }}" style="height:100px; width:100px; margin:10px" alt="Card image cap">
                                            <p class="card-text">{{ subcommittee-member.bio }}</p>
                                    </div>
                                </div>
                            </div>
                         {% endif %}
                    {% endfor %}
                 </div><br>
                {% endfor %}
            </div>
        </div>
    </div>
</section>

    
	
