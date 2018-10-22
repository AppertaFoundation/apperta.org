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

<section id="openEHR-templatess">
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
                <th>Key Words</th>
            </tr>
        </thead>
        <tbody>
        {% for openEHR-templates in site.openEHR-templates %}
            <tr>
                <td style="text-align:center; vertical-align:middle">{{ openEHR-templates.name }}</td>
                <td><p>{{ openEHR-templates.description }}</p></td>
                <td style="text-align:center; vertical-align:middle">{{ openEHR-templates.lead }}</td>    
            <td style="text-align:center; vertical-align:middle">{{ openEHR-templates.status }}</td>  
                <td style="text-align:center; vertical-align:middle">
                {% if openEHR-templates.ckm == null %}
                {% else %}
                {% if openEHR-templates.ckm contains 'http' %}  
                <a href="{{ openEHR-templates.ckm }}" target="_blank"><i class="fas fa-globe fa-2x"></i></a>
                {% else %} 
                <a href="{{ openEHR-templates.ckm }}"><i class="fas fa-globe fa-2x"></i></a>
                {% endif %}
                {% endif %}
                </td>
                <td style="text-align:center; vertical-align:middle">
                {% if openEHR-templates.git == null %}
                </td>
                {% else %}
                <a href="{{ openEHR-templates.git }}" target="_blank"><i class="fab fa-github fa-2x"></i></a>
                {% endif %}
                </td>
                <td>{{ openEHR-templates.keywords }}</td>
            </tr>
        {% endfor %}
    </tbody>
</table>
</div>        
      </div>
	  </div>
	  </div>
    </section>
