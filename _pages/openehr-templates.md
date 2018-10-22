---
permalink: "/openEHR-templates/"
layout: page
title: "openEHR Templates"
---

<section class="bg-primary text-white" id="about">
      <div class="container text-center">
        <h2 class="mb-4">Clinical Content</h2>
        <p align="left">Introduction</p><br>
		<center><a class="btn btn-light btn-xl" href="mailto:info@apperta.org">Suggest a Template</a></center>
</div>
</section>

<section id="openEHR-templates">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <center><h2 class="section-heading">openEHR Templates</h2>
            <hr class="my-4"></center>

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
                <!--hidden field-->
                <th>Key Words</th>
            </tr>
        </thead>
        <tbody>
        {% for openEHR-template in site.openEHR-templates %}
            <tr>
             <!--Template Name -->
                <td style="text-align:center; vertical-align:middle">{{ openEHR-template.name }}</td>
            <!--Template Description-->
                <td><p>{{ openEHR-template.description }}</p></td>
            <!--Template Clinical Lead-->
                <td style="text-align:center; vertical-align:middle">{{ openEHR-template.lead }}</td>  
            <!--Template Status-->    
            <td style="text-align:center; vertical-align:middle">{{ openEHR-template.status }}</td>  
            <!--Template CKM Link-->
                <td style="text-align:center; vertical-align:middle">
                {% if openEHR-template.ckm == null %}
                {% else %}
                {% if openEHR-template.ckm contains 'http' %}  
                <a href="{{ openEHR-template.ckm }}" target="_blank"><i class="fas fa-globe fa-2x"></i></a>
                {% else %} 
                <a href="{{ openEHR-template.ckm }}"><i class="fas fa-globe fa-2x"></i></a>
                {% endif %}
                {% endif %}
                </td>
            <!--Template Git Link-->
                {% if openEHR-template.git == null %}
                <td></td>
                {% else %}
                <td style="text-align:center; vertical-align:middle"><a href="{{ openEHR-template.git }}" target="_blank"><i class="fab fa-github fa-2x"></i></a></td>
                {% endif %}
            <!--Template Keywords HIDDEN-->
                <td>{{ openEHR-template.keywords }}</td>
            </tr>
        {% endfor %}
    </tbody>
</table>
</div>

        
      </div>
	  </div>
	  </div>
    </section>
