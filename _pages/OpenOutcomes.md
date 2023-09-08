---
permalink: "/openOutcomes/"
layout: singlePage
title: "OpenOutcomes"
description: 
TOR: '/assets/Open Outcomes - Community Update (230120).pdf'
---

<section class="bg-white text-black" id="about">
        <div class="container text-left">
        <h1 class="text-uppercase text-dark text-center">{{ page.title }}</h1><br>
        <h2 align="center">Background</h2><br>
        <hr class="mb-4">
        <p>Musculoskeletal interventions including physiotherapy, orthotics and surgery always have an impact on patients, hopefully for the better, sometimes for the worse. There is variability in outcomes, which can depend on patient factors but can also depend on the teams delivering care to patients. So that any variability in outcomes in patient groups can be studied and improvements in care made, ‘Outcome Measures’ are collected. These are often patient completed questionnaires to formally score patients’ pain and function before and after interventions including physiotherapy and surgery. Patient Reported Outcome Measures are known as PROMs.</p> 

<p>Some healthcare providers and registries now routinely collect questionnaires to compare patients’ pre and post-intervention scores to inform clinical practice and drive improvement (Figure 1). The questionnaires are normally specific to the intervention that has been performed (e.g., hip and knee replacement scores) and most operations or interventions will also have a more general health status score applied (commonly the EuroQol 5 domain general health questionnaire, the “EQ-5D”). EQ-5D can be applied across all aspects of healthcare and is a good way to work out how much impact an intervention or operation may have on health compared to say treatment for diabetes. Other general questionnaires such as the MSK-HQ are being increasingly used in primary care and physiotherapy settings. This helps healthcare providers direct resources to the interventions that have the most patient benefit.</p>

<p>Healthcare organisations currently collect the data mostly in paper format which is then converted into an electronic format for storage and analysis purposes (usually via manual input).</p>

<p>We have chosen to develop a solution that will be open source and based on open standards. It sits either in fully compliant cloud-based servers or within a healthcare organisation’s own environment, meeting all industry standards for security and GDPR. All data collected via the software is held in an open computable format (openEHR) which facilitates data analytics and is designed to interoperate with other healthcare digital systems (Figure 2). Healthcare organisations have full real-time access to their patient data for analysis and other uses (Figure 1), and data is protected as per the NHS governance policies.</p> 


<img src="/img/OO-figure-1.png" width="100%"><br>

<i><b>Figure 1:</b> The many uses of PROMs using the openOutcomes digital platform. </i><br><br>

<h2 align="center">Solution</h2>
<hr class="mb-4">
<p>There are commercial options available; these can routinely cost each NHS organisation up to £50,000 per year. Instead, we can do this collectively, reduce cost and deliver a best-in-class solution designed by its users. To take the work forward we have created a committee under the governance of The Apperta Foundation, allowing others to get involved and collectively fund the product build. The Apperta Foundation is a clinician-led, “not-for-profit" and is supported by NHS England, NHS Digital and others. We estimate future costs to be £15k 'one off' implementation per trust/hospital and approximately £20-25k per annum. for annual support, hosting, maintenance and membership of the leadership committee deciding future functionality. The more Trusts, Health Boards and organisations that join us, the cheaper it will get. We are happy to work with the independent sector, and overseas organisations</p>

<h2 align="center">Progress to Date </h2>
<hr class="mb-4">
<p>We have been successful with obtaining funding from NHS Transformation (formerly NHSx) via the MSK Adoption Fund along with funding from the North of England Commissioning Support unit (NECS) to build a best-in-class solution PROMs platform. We have completed the core minimum viable product (MVP) for the openOutcomes platform which can read and pull patient demographics from PAS and allow staff access via Active Directory (using their hospital password). This is being integrated into two NHS Trusts (Northumbria Healthcare and Birmingham and Sandwell) for testing and feedback before offering the platform to further trusts subscribed to the project.</p>

<p>The platform has been designed to be “pathway agnostic” and cover PROMs in any specialty, as well as Patient Reported Experience Measures (PREMs). Common MSK and Orthopaedic outcomes have long been championed and questionnaires have now been written as openEHR archetypes ready to be incorporated into the platform should Trusts require it. These include:</p>

<ul align="left">
    <li>Foot & Ankle – MOXFQ, AOS, AOFAS, SAFAS, VISA-A, ATRS </li>
    <li>Upper Limb – OSS, OSIS, OES, Boston, PEM, URAM, QDash </li>
    <li>Hip – OHS, iHOT12, NAHS </li>
    <li>Spine – NDI, MDI, ODI, VAS back & leg, VAS arm & neck </li>
    <li>Knee – OKS, OKS (A&P), KOOS, Tegner, IKDC </li>
    <li>General MSK – MSK HQ </li>
    <li>General health– EQ-5D,  </li>
    <li>Pain VAS,  </li>
    <li>Patient Satisfaction </li>
</ul>

<p>Current PROMS input methods include:</p> 
<ul align="left">
    <li>Paper, supported by administrator input (currently the best method to get patient engagement with rates around 50%) </li>
    <li >Electronic entry (currently the cheapest method to collect data, but with maximum reach around 25%) </li>
    <li>Tablets or PC web browser entry by the patients in clinic within the hospital’s intranet </li>
    <li>Web and smartphone / tablet entry via the public internet </li>
    <li>The software has automatic prompts when post-operative responses are due and prompts when questionnaires have not been received. </li>
</ul>

<p>Multilingual support is planned.</p>

<p>openOutcomes has the ability to analyse PROMs data and view charts, graphs, and tables with a variety of queries possible. This allows real time data to be available to clinicians and teams within the NHS organisation using it. Furthermore, OpenOutcomes records data about the procedure itself which can be passed along with the PROMs data into analysis tools with a range of purposes including correlational analysis, creation of visualisations and machine learning.</p> 

<p>Shortly we will have the ability to push data into national registries to avoid duplication and save time.</p>

<p>Future aims, should further funds become available and subject to the decisions of the committee, might include:</p>
<ul align="left">
    <li>The ability for the software to generate bar coded questionnaires so they can be automatically posted out to patients and automatically read when returned and ascribed to the correct patient and operation/intervention. </li>
    <li>Voice generated PROMS scores from robot generated phone calls. </li>
</ul>

<p>OpenOutcomes is a digital platform capable of building on modules for other speciality PROMs such as ophthalmology, general surgery and cancer services. The technology upon which its built allows for any PROMs questionnaire to be incorporated into the platform due its agnostic capabilities. Figure 2 shows the high level overview of the data technology architecture and how it can interoperate with other digital systems and EPRs within and across NHS organisations.</p>

<img src="/img/OO-figure-2.png" width="100%"><br>

<i><b>Figure 2:</b> High level data architecture overview of openOutcomes and how it is interoperable with other IT system across the NHS (Diagram adapted from John Meredith, NHS Wales) </i><br><br>

<div class="container">
    <center>
        <h2 class="mb-4">Demonstration Videos</h2>
        <hr class="mb-4">
    </center>
    <div class="row">
        <div class="col-lg-6 mb-4">
            <div class="card h-100">
                <div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/851914248?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Introduction to Open Outcomes"></iframe></div>
            </div>
        </div>
        <div class="col-lg-6 mb-4">
            <div class="card h-100">
                <div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/847937935?title=0&byline=0&portrait=0&speed=0&badge=0&autopause=0&player_id=0&app_id=58479/embed" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen frameborder="0" style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe></div>
            </div>
        </div>
    </div>
    <div class="row">
        <div class="col-lg-6 mb-4">
            <div class="card h-100">
                <div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/860126029?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Open Outcomes - Patient Experience"></iframe></div>
            </div>
        </div>  
        <div class="col-lg-6 mb-4">
            <div class="card h-100">
                <div style="padding:56.37% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/795709502?title=0&byline=0&portrait=0&speed=0&badge=0&autopause=0&player_id=0&app_id=58479/embed" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen frameborder="0" style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe></div>
            </div>
        </div>
    </div>
</div>

<h2 align="center">Over to you </h2>
<hr class="mb-4">

<p>We want clinicians, allied healthcare professionals and their departments to get involved in this exciting project by subscribing to use the product and help to shape its future. Subscribers will be asked to take a seat on our committee if they so wish, to govern product development and to decide how future investment should be spent.</p>
<center>
<div class="row">
                <div class="col-sm-6">
                    <a href="/assets/openOutcomes%20Frequently%20Asked%20Questions.pdf"><img src="/img/oo-faq.png"></a><br>
                   <font size="2"><p>Read our <b>Frequently Asked Questions</b> to aid any departmental discussions</p></font>
                </div>
                <div class="col-sm-6">
                    <a href="/assets/openOutcomes%20Executive%20summary.pdf"><img src="/img/executive-summary.png"></a>
                    <font size="2"><p>Download our <b>Executive Summary</b> to share with your colleagues.</p></font>
                </div>
            </div>
        <br>
        <a class="btn btn-primary btn-xl" href="mailto:info@apperta.org?Subject=%5BOpenOutcomes">Get in Touch</a></center></div>
</section>

<section id="about" style="background-image:url(../img/blog-bg_blue.png);background-position:center center;-webkit-background-size:cover;-moz-background-size:cover;-o-background-size:cover;background-size:cover">
      <div class="container">
          <div class="col-lg12 mx-auto text-center">
            <h1 class="text-uppercase text-dark">
              <strong>Committee</strong>
            </h1>
            <h2 class="section-heading text-white">Our Committee Members</h2>
                {% assign members = site.subcommittee-members | where:"subcommittee",page.title %}
                {% assign rows = members.size | divided_by: 3.0 | ceil %}
                {% for i in (1..rows) %}
                <div class="row">
                    {% assign offset = forloop.index0 | times: 3 %}
                     {% assign sorted = site.subcommittee-members | where:"subcommittee",page.title | sort:"position" %}
                       {% for subcommittee-member in sorted limit:3 offset:offset%} 
                        {% if subcommittee-member.subcommittee == page.title %}
                            <div class="col-sm-4">
                                <div class="card" style="height: 100%;">
                                    <div class="card-header"><strong>{{ subcommittee-member.name }}</strong> <p><em>{{ subcommittee-member.role }}</em> </p>
                                    </div>
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

