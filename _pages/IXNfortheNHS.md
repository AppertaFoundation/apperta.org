---
permalink: "/IXNfortheNHS/"
layout: singlePage
title: "Industry Exchange Network (IXN) for the NHS"
description: <p align="left">The Power of Collaboration - pairing Computer Science Education and Technology with Clinicians to strengthen and enhance the NHS.</p><p align="left">Launched in February 2019, the Industry Exchange Network (IXN) for the NHS committee has been established to allow Industry, Educators, Researchers and Clinicians to work together to advance the UK's healthcare through Interoperability, Efficiency and Innovation (IEI) open source projects.</p><p align="left">The Chair of the IXN for the NHS committee is Dean Mohamedally, a Principal Teaching Fellow at the Department of Computer Science at University College.  Dean pioneered the concept of the industry exchange network in the Department of Computer Science at University College London where it has been in operation for over seven years working with NHS trusts.</p><p align="left">The Committee will work to promote open systems and standards across the NHS in the form of an industry exchange network, as requested by Government in the Topol Review. We have been and still are leading the way with Machine Learning Readiness tasks for clinical groups. We are overseeing the largest training environment in the world for FHIR (Fast Healthcare Interoperability Resource) and OpenEHR (Open Electronic Healthcare Records) projects. Our students are pushing the boundaries of technology applied to modern medicine and patient care.</p><p align="left">This committee will oversee and curate student projects with technology providers and clinical groups that have open IT systems, shareable components and computable algorithms. This will</p><ul><li align="left">Proceed with building necessary systems architectures, platforms, APIs and components for adopting standards, specifically for interoperability validation of successful systems integration in healthcare</li><li align="left">Identify weaknesses in current health service strategies, collecting classifications of requested optimisations, and improve both local and general efficiency of existing services with the advantages that technology can bring</li><li align="left">facilitate the creation of innovation in digital health to transform the delivery of health and social care with AI and Machine Learning, Data Science, Computer Vision and the latest state of the art in technology development</li></ul><p align="left">There are many problems in healthcare to solve, big and small, and engineering students must publish their work to be seen. This is a partnership programme that lets students become the best they can be with real world requirements, and clinicians exploring the best and latest technologies that industry can provide.</p>
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
              <strong>Committee</strong>
            </h1>
            <h2 class="section-heading text-white">Our Committee Members</h2>
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
