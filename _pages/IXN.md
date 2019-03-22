---
permalink: "/IXN/"
layout: singlePage
title: "Industry Exchange Network for the NHS (IXN)"
description: <p>On 14th February 2019 we launched a UK-wide industry exchange network (IXN) for the NHS. The initiative will provide a solution and home to two of the most pressing challenges facing the NHS - how do we start to build a future facing NHS workforce, and, how do we identify and design healthcare technologies that truly meet local and national healthcare needs?</p><p>The IXN for the NHS is rooted in the concept pioneered by the Department of Computer Science at University College London where it has been in operation for over 7 years.  Over 500 candidates (undergraduate and Masters level) work on different levels and scales of real- world computer science problems every year.  The initiative is supported by over 300 industry partners such as Microsoft, NTT Data and IBM.  Outputs are proof of concepts which can be progressed if considered to be of true benefit to the health and care ecosystem.</p><p>The Apperta Foundation has worked with UCL for several years and has facilitated over 200 projects for students to work with a Code4Health NHS mentor and industry partner. Many student projects conceived and developed have already been contributors to NHS technologies (from mental health chatbots, to a web-based treatment and management system for hepatitis C, and machine learning readiness tasks for clinicians.</p><p>Following the example of the UCL Computer Science industry exchange network model, the IXN for the NHS will provide a framework for other UK universities and industry partners to contribute, with their STEM (science, technology, engineering and mathematics) programmes working on projects with the NHS. The IXN for the NHS will have a grounded centre to facilitate interoperability, efficiency and innovation. However, this initiative needs to be allied with NHS career paths for STEM students who want to continue working in/with the NHS, having been introduced to this through the industry exchange network.</p>
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
        <div class="row">
          <div class="col-lg12 mx-auto text-center">
            <h1 class="text-uppercase text-dark">
              <strong>Subcommittee</strong>
            </h1>
            <h2 class="section-heading text-white">Our Subcommittee Members</h2>
            <hr class="light my-4">
                <div class="row">
{% assign rows = site.subcommittees.size | divided_by: 3.0 | ceil %}
{% for i in (1..rows) %}

  <div class="row" style="margin-top: 20px">

  {% assign offset = forloop.index0 | times: 3 %}
  {% for subcommittee in site.subcommittees limit:3 offset:offset %}
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
                                            </div><br>                                         
                                    </div>
                                </div>
                            </div><br><br>
                                 {% endif %}
                             {% endfor %}
                        </div>
                        {% endfor %}
            </div>
        </div>
    </div>
</section>