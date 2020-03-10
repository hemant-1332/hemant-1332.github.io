---
layout: page
title: Hi, I'm Hemant
subtitle: Software Developer | An Engineer | Love to learn about Universe !
css: "/css/index.css"
meta-title: "Hemant Singh - SDE"
meta-description: "Software developer"
datacampcourse: false
bigimg:  
  - "/img/timeline/cruise.jpg" : "Halong Bay, Vietnam (2018)"
  - "/img/timeline/cruise-meal.jpg" : "Halong Bay, Vietnam (2018)"
  - "/img/timeline/daewoo-hotel.jpg" : "Hanoi, Vietnam (2018)"
  - "/img/timeline/delhi-wedding.jpg" : "New Delhi (2020)"  
  - "/img/timeline/landmark72-hanoi.jpg" : "Hanoi, Vietnam (2018)"  
  - "/img/timeline/tibba.jpg" : "Himachal (2018)"  
  - "/img/timeline/vietnam-1.jpg" : "Hanoi, Vietnam (2018)"
  - "/img/timeline/vietnam-2.jpg" : "Hanoi, Vietnam (2018)"  
---

<div class="list-filters">
  <a href="/" class="list-filter">All posts</a>
  <!-- <a href="/popular" class="list-filter">Most Popular</a> -->
  <span class="list-filter filter-selected">Tutorials</span>
  <a href="/tags" class="list-filter">Index</a>
</div>

<div class="posts-list">
  {% for post in site.tags.tutorial %}
  <article>
    <a class="post-preview" href="{{ post.url | prepend: site.baseurl }}">
	    <h2 class="post-title">{{ post.title }}</h2>
	
	    {% if post.subtitle %}
	    <h3 class="post-subtitle">
	      {{ post.subtitle }}
	    </h3>
	    {% endif %}
      <p class="post-meta">
        Posted on {{ post.date | date: "%B %-d, %Y" }}
      </p>

      <div class="post-entry">
        {{ post.content | truncatewords: 50 | strip_html | xml_escape}}
        <span href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</span>
      </div>
    </a>  
   </article>
  {% endfor %}
</div>
