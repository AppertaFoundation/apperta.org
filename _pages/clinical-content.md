---
permalink: "/clinical-content/"
layout: singlePage
title: "Clinical Content"
description: The Clinical Content Subcommittee is a group of clinicians and experienced professionals from appropriate specialities and backgrounds. The Subcommittee includes representatives from England, Scotland, Ireland, Northern Ireland and Wales. The primary purpose of the Subcommittee is to drive and influence the development and quality improvement of open and shared clinical content for eHealth projects via a collaborative community, and to encourage and facilitate its use in real e-health implementations. They will provide the technical tools, plus professional support and assurance to those responsible for and involved in e-health projects where clinical content is a factor. The Subcommittee will work to promote open systems and standards for digital health and social care. They will support the aim to make the data, information and knowledge within IT systems open, shareable and computable. This will facilitate the creation of innovative digital services to transform the delivery of health and social care. The Subcommittee is chaired by a qualified and practising health professional, and consists of members with the appropriate skills and experience to enable them to contribute to the development of the clinical content agenda and influence how it progresses on behalf of their nation.
TOR: '/assets/Apperta-CCSubComm-TOR.pdf'
---

<section class="bg-white text-black" id="about">
      <div class="container text-center">
        <h1 class="text-uppercase text-dark">{{ page.title }}</h1><br>
        <p align="left">{{ page.description }}</p><br>
        <p align="left">The subcommittee has curated a number of openEHR templates for us which can be found <a href="{{ '/openEHR-templates' }}">here</a>.</p><br>
        <p align="left">A copy of the subcommittee terms of reference can be found <a href="{{ page.TOR }}">here.</a></p><br>
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
                {% assign rows = site.subcommittee-members.size | where:"subcommittee",page.title | divided_by: 3.0 | ceil %}
                {% assign check = site.subcommittee-members | where:"subcommittee",page.title %}
                {% assign checkrows = check.size | divided_by: 3.0 | ceil %}
                <p>
                    ROWS: 
                    {{ checkrows  }}
                </p>
                {% for i in (1..rows) %}
                <div class="row">
                    {% assign offset = forloop.index0 | times: 3 %}
			         {% assign sorted = site.subcommittee-members | sort:"role" %}
                       {% for subcommittee-member in sorted limit:3 offset:offset%} 
                        {% if subcommittee-member.subcommittee == page.title %}
                            <div class="col-sm-4">
                                <div class="card" style="height: 100%;">
                                    <div class="card-header"><strong>{{ subcommittee-member.name }}</strong> <p><em>{{ subcommittee-member.role }}</em> </p></div>
                                    <div class="card-body">
                                        <img class="pull-left" src="{{ subcommittee-member.photo }}" style="height:100px; width:100px; margin:10px" alt="Card image cap">
                                            <p class="card-text">{{ subcommittee-member.bio }}</p>
                                            <div class="row">
                                                <div class="col-md-12 col-xs-12 col-centered">                        {% if subcommittee-member.twitter == null %}
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

    
	
