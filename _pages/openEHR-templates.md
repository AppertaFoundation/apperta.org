---
permalink: "/openEHR-templates/"
layout: singlePage
title: "openEHR Templates"
---
<section class="bg-primary text-white" id="about">
      <div class="container text-center">
        <h2 class="mb-4">Clinical Content</h2>
        <h3 class="mb-4">openEHR Templates</h3>
        <hr class="my-4">
        <p align="left">Templates are used to create definitions of content such as a particular document or message, required for specific use cases, such as specific screen forms, message types or reports. Typical examples include 'acute care discharge summary', 'GP referral' and radiology report'.  A list of the openEHR templates curated by the Clinical Content subcommittee can be found below.</p><br>
		<!--<center><a class="btn btn-light btn-xl" href="mailto:info@apperta.org">Suggest a Template</a></center>-->
    </div>
</section>
<section id="openEHR-templates">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
           <!--<center><h2 class="section-heading">openEHR Templates</h2>
            <hr class="my-4"></center>-->
  	<div style="overflow-x:auto;">	
         <table id="project" class="table table-striped table-bordered display responsive no-wrap" style="width:100%">
        <thead>
            <tr>
                <th>Template Name</th>
                <th>Description/Use</th>
                <th>Clinical Lead</th>
				<th>Status</th>
                <th>CKM Link</th>
                <th><i class="fab fa-github"></i> Git Location</th>
                <th>Exemplar Application</th>
                <th>Key Words</th>
            </tr>
        </thead>
        <tbody>
        {% for templates in site.openEHR-templates %}
            <tr>
                <td style="text-align:center; vertical-align:middle">{{ templates.name }}</td>
                <td><p>{{ templates.description }}</p></td>
                <td style="text-align:center; vertical-align:middle">{{ templates.lead }}</td>    
            <td style="text-align:center; vertical-align:middle">{{ templates.status }}</td>  
                <td style="text-align:center; vertical-align:middle">
                {% if templates.ckm == null %}
                {% else %}
                <a href="{{ templates.ckm }}"><i class="fas fa-globe fa-2x"></i></a>
                {% endif %}
                </td>
                <td style="text-align:center; vertical-align:middle">
                {% if templates.git == null %}
                </td>
                {% else %}
                <a href="{{ templates.git }}" target="_blank"><i class="fab fa-github fa-2x"></i></a>
                {% endif %}
                </td>
                <td style="text-align:center; vertical-align:middle">
                {% if templates.exemplar == null %}
                {% else %}
                <a href="{{ templates.exemplar }}" target="_blank">{{ templates.examplar-name }}</i></a>
                {% endif %}
                </td>
                <td>{{ templates.keywords }}</td>
            </tr>
        {% endfor %}
    </tbody>
</table>
</div>        
      </div>
	  </div>
	  </div>
    </section>
