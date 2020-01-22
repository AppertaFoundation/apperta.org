---
permalink: "/OpenOutcomes/"
layout: singlePage
title: "Open Outcomes"
description: <p align="left">Background</p><p align="left">Operations on patients always have an impact, hopefully for the better, sometimes for the worse. There is variability in outcomes, which can depend on patient factors but can also depend upon the surgical teams that perform the surgery. So that any variability in outcomes in patient groups can be studied and improvements in care made, ‘Outcome Measures’ are collected. These are often patient completed questionnaires to formally score patients pain and function before and after surgery. Patient Reported Outcome Measures are known as PROMs.</p>
TOR: 
---

<section class="bg-white text-black" id="about">
      <div class="container text-center">
        <h1 class="text-uppercase text-dark">{{ page.title }}</h1><br>
        <p align="left">{{ page.description }}</p><br>
        <!--<p align="left">A copy of the subcommittee terms of reference can be found <a href="{{ page.TOR }}">here.</a></p><br>-->
        <center><a class="btn btn-primary btn-xl" href="mailto:info@apperta.org?Subject=%5BClinical%20Content%20Subcommittee">Get in Touch</a></center>
    </div>
</section>
<section id="about" style="background-image:url(../img/blog-bg_blue.png);background-position:center center;-webkit-background-size:cover;-moz-background-size:cover;-o-background-size:cover;background-size:cover">
      <div class="container">
          <div class="col-lg12 mx-auto text-center">
            <h1 class="text-uppercase text-dark">
              <strong>Subcommittee</strong>
            </h1>
            <h2 class="section-heading text-white">Our Subcommittee Members</h2>
            <hr class="light my-4">
                
                {% assign members = site.subcommittee-members | where:"subcommittee",page.title %}
                {% assign rows = members.size | divided_by: 3.0 | ceil %}
                {% for i in (1..rows) %}
                <div class="row">
                    {% assign offset = forloop.index0 | times: 3 %}
                     {% assign sorted = site.subcommittee-members | where:"subcommittee",page.title | sort:"role" %}
                       {% for subcommittee-member in sorted limit:3 offset:offset%} 
                        {% if subcommittee-member.subcommittee == page.title %}
                            <div class="col-sm-4">
                                <div class="card" style="height: 100%;">
                                    <div class="card-header"><strong>{{ subcommittee-member.name }}</strong> <p><em>{{ subcommittee-member.role }}</em> </p></div>
                                    <div class="card-body">
                                        <img class="pull-left" src="{{ subcommittee-member.photo }}" style="height:100px; width:100px; margin:10px" alt="Card image cap">
                                            <p class="card-text">{{ subcommittee-member.bio }}</p>
                                            <div class="row">
                                                <div class="col-md-12 col-xs-12  col-centered">                        {% if subcommittee-member.twitter == null %}
                                                    {% else %}
                                                    <a href="http://twitter.com/{{ subcommittee-member.twitter }}" target="_blank"><i class="fab fa-twitter fa-2x"></i></a>
                                                {% endif %}
                                                {% if subcommittee-member.www == null %}
                                                    {% else %}
                                                    <a href="{{ subcommittee-member.www }}" target="_blank"><i class="fas fa-globe fa-2x"></i></a>
                                                {% endif %}
                                                {% if subcommittee-member.linkedin == null %}
                                                    {% else %}
                                                    <a href="{{ subcommittee-member.linkedin }}" target="_blank"><i class="fab fa-linkedin fa-2x"></i></a>
                                                {% endif %}
                                                {% if subcommittee-member.github == null %}
                                                    {% else %}
                                                    <a href="{{ subcommittee-member.github }}" target="_blank"><i class="fab fa-github fa-2x"></i></a>
                                                {% endif %}
                                                </div>
                                            </div>                                         
                                    </div>
                                </div>
                            </div>
                         {% endif %}
                    {% endfor %}
                 </div><br>
                {% endfor %}
            </div>
        </div>  
</section>
