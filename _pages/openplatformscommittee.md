---
permalink: "/openplatformscommittee/"
layout: singlePage
title: "Open Platforms"
description: <b>We are pleased to announce that the chair of the Open Platforms Committee has rotated to Dr Paul Miller as Clinical Co-Chair and John Meredith as Technical Co-Chair, we would like to thank both Dr Shane McKee and Dr Alistair Walling for their time and hard work in those roles and who remain active members of the Committee.</b><br><br>The Open Platform Committee is a group of clinicians and experienced professionals from appropriate specialities and backgrounds.<br><br>The Committee includes representatives from England, Scotland, Northern Ireland and Wales.<br><br>The purpose of the Open Platform Committee is to drive and influence the development and quality improvement of open and shared clinical content and curate the architecture of open platforms for eHealth projects via a collaborative community. The Committee will encourage and facilitate their use in real world implementations.<br><br>They will provide the technical tools, plus professional support and assurance to those responsible for and involved in projects where clinical content is a factor. The Committee will promote open systems and standards for digital health and social care. They will support the aim to make the data, information and knowledge within IT systems open, shareable and computable. This will facilitate the creation of innovative digital services to transform the delivery of health and social care.<br><br>The Committee will ensure exemplar open platform is maintained, based on the “Defining an Open Platform” publication for use in development, test and demonstration of digital health solutions; it will provide professional support and assurance to those involved in digital health and care projects.<br><br>The Committee is jointly chaired by a qualified and practising health professional and a non-clinical health informatics professional. The Committee consists of members with the appropriate skills and experience to enable them to contribute to the development of the Open Platform agenda and influence how it progresses on behalf of the health and care system.
TOR: '/assets/Apperta-TOR-OPlatform-v1.0.pdf'
---

<section class="bg-white text-black" id="about">
      <div class="container text-center">
        <h1 class="text-uppercase text-dark">{{ page.title }}</h1><br>
        <p align="left">{{ page.description }}</p><br>
        <p align="left">The committee has curated a number of openEHR templates for us which can be found <a href="https://github.com/AppertaFoundation/apperta-uk-ckm-mirror/tree/master" target="_blank">here</a>.</p><br>
        <p align="left">A copy of the committee terms of reference can be found <a href="{{ page.TOR }}">here.</a></p><br>
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
