---
permalink: "/openOutcomes/"
layout: singlePage
title: "OpenOutcomes"
description: 
TOR: '/assets/Open Outcomes - Community Update (230120).pdf'
---

<section class="bg-white text-black" id="about">
      <div class="container text-center">
        <h1 class="text-uppercase text-dark">{{ page.title }}</h1><br>
        <p align="left">
        <h2>Background</h2>
        <p align="left">Operations on patients always have an impact, hopefully for the better, sometimes for the worse. There is variability in outcomes, which can depend on patient factors but can also depend upon the surgical teams that perform the surgery. So that any variability in outcomes in patient groups can be studied and improvements in care made, ‘Outcome Measures’ are collected. These are often patient completed questionnaires to formally score patients pain and function before and after surgery. Patient Reported Outcome Measures are known as PROMs.
        </p>
        <p align="left">Some trusts now routinely collect questionnaires to compare patients’ pre-operative and post-operative scores to inform clinical practice and drive improvement. The questionnaires are normally specific to the operation that has been performed (e.g. knee replacement scores, or hernia scores) and most operations will also have a more general health status score applied as well (known as EQ-5D). EQ-5D can be applied across all aspects of healthcare and is a good way to work out how much impact an operation may have on health compared to say treatment for diabetes. This helps healthcare providers direct money to the interventions that have the most patient benefit.</p>
        <p align="left">Trusts currently collect the data in paper format which is then converted into an electronic format for storage and analysis purposes (usually via manual input).</p>
        <p align="left">We have chosen to develop a solution will be open source and based on open standards. It will sit either in fully compliant cloud-based servers or could sit within a trust’s own environment meeting all industry standards for security and GDPR. All data collected via the software will be held in an open computable format (openEHR) which will facilitate data analytics and will be designed to interoperate with other hospital systems. Trusts have full real time access to their patient data for analysis, data is protected as per the trusts governance policies.</p>
        <p align="left"><h2>Our Ask</h2></p>
        <p align="left">There are commercial options available, these routinely cost each NHS trust up to £50,000 PA. Instead, we can do this collectively, reduce cost and deliver a best in class solution designed by its users. To take the work forward we have created a Committee under the governance of the Apperta Foundation. We are asking others to get involved and commit to a minimum £5000 annual subscription. Our target is to raise £100,000, when we reach £50,000 we will start our build.</p>
        <p align="left"><h2>Progress to Date</h2></p>
        <p align="left">We’ve created an alpha solution with support from the Code4Health initiative and its partners. This has basic functionality for inputting patient and procedure data using Foot & Ankle as the use case and was tested internally at Northumbria Healthcare. There is also the facility for a basic data export into Excel for analysis.</p>
        <p align="left"><h2>Next Steps</h2></p>
        <p align="left">We are now ready to move forward; the next phase will add other specialty modules and further functionality.</p>
        <p align="left">Orthopaedic questionnaires which have now been written as archetypes ready to be incorporated into the platform are...</p>
        <ul>
            <li align="left">Foot & Ankle – MOXFQ, AOS, AOFAS, SAFAS, VISA-A, ATRS</li>
            <li align="left">Upper Limb – OSS, OSIS, OES, Boston, PEM, URAM, QDash</li>
            <li align="left">Hip – OHS, iHOT12, NAHS</li>
            <li align="left">Spine – NDI, MDI, ODI, VAS back & leg, VAS arm & neck</li>
            <li align="left">Knee – OKS, OKS (A&P), KOOS, Tegner, IKDC</li>
            <li align="left">General MSK - MSKHQ</li>
            <li align="left">General health– EQ-5D, Pain VAS, Patient Satisfaction</li>
        </ul>
        <p align="left">We plan to add several other features, including...</p>
        <p align="left"><h3>Additional methods to input outcomes</h3></p>
        <ul>
            <li align="left">Tablets or PC browser entry by the patients in clinic within the hospital’s intranet</li>
            <li align="left">Web and smartphone / tablet entry via the internet</li>
            <li align="left">Text responses</li>
            <li align="left">The ability for the software to generate bar coded questionnaires so they can be automatically posted out to patients and automatically read when returned and ascribed to the correct patient and operation/intervention.</li>
        </ul>
        <p align="left"><h3>Additional functionality</h3></p>
        <ul>
            <li align="left">Automatic prompts when post-operative responses are due</li>
            <li align="left">Prompts when questionnaires have not been received</li>
            <li align="left">Reporting module</li>
            <li align="left">Ability to analyse data and view charts, graphs, and tables with a variety of queries possible. This will allow real time data to be available to clinicians and teams within hospitals.</li>
            <li align="left">Data push into national registries</li>
            <li align="left">Ability to push data into the various national registries to avoid duplication and save time.</li>
        </ul>
        <p align="left"><h2>Over to you</h2></p>
        <p align="left">We want clinicians and their departments to get involved, subscribe to use the product and help to shape its future. Subscribers will be asked to take a seat on our committee if they so wish, to govern product development and to decide how future investment should be spent.</p></p><br>
        <p align="left">We have produced a FAQ to aid with any departmental discussions, download it here <a href="assets/openOutcomes Frequently Asked Questions.pdf">Frequently asked questions</a></p>
        <p align="left">A copy of our recent committee update can be found <a href="{{ page.TOR }}">here.</a></p><br>
        <center><a class="btn btn-primary btn-xl" href="mailto:info@apperta.org?Subject=%5BOpenOutcomes">Get in Touch</a></center>
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
