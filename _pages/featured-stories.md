---
permalink: "/featured-stories/"
layout: singlePage
title:  "Featured Stories"
---



<section class="text-white" id="news" style="background-color:#1a5281">
      <div class="container text-center">
      <div class="col-lg-10 mx-auto">
              <h1 class="mb-4">All Stories</h1>
            </div>
          </div>
        </section>

  <section>
  <div class="container">



        <div class="row "> 
              <div class="row" id="stories">
               {% for post in site.posts %}
                <div class="col-md-4" style="padding:10px">
                  <div class="thumbnail">
                  <a href="{{ post.url }}">
                  <img  src="{{ post.thumbnail }}" style="width:80%" alt="{{ post.title }}">
                  <div class="caption text-dark"><br>
                    <p>{{ post.title }}</p> 
                  </div>
                  </a>
                </div>
                </div>
              {% endfor %}
              </div>
        </div>
        </div>
</section>
  