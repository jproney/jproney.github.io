---
layout: nofoot
---
{% include custom-head.html %}
<div class="flex-container">
  <div class="flex-vertical">
  <img src="images/me.png" alt="Profile Picture" class="profile-pic" >

  <div class="iconbar">
  <a href="https://github.com/jproney">
  <img src="images/github-mark.png" class=social></a>
  <a href="https://linkedin.com/in/james-p-roney">
  <img src="images/linkedin.png" class=social></a>
  <a href="https://scholar.google.com/citations?user=Yi5_KxgAAAAJ&hl=en">
  <img src="images/scholar.png" class=social></a>
  <a href="mailto:jamesproney@gmail.com">
  <img src="images/mail.png" class=social></a>
  </div>

  </div>
  <div class="bio">
    <h1>Hi, I'm James Roney.</h1>
    <p>
I'm currently a Research Engineer at <a href="https://www.deshawresearch.com"> DE Shaw Research</a> in New York, where I work on problems at the intersection of machine learning  and drug discovery. I graduated from Harvard in 2022, where I did research on various topics in computer science, statistics, and biology. I'm broadly interested in applying computational methods to problems involving biological structure. My specific areas of interest include the use of machine learning to help with protein structure modeling, protein design, structure-based drug design, and molecular simulation.
    </p>
  </div>
</div>
<br>


<br>

# **Publications**

{% assign publications = site.publications | sort: "year" | reverse %}
{% for pub in publications %}
<div class="pubitem">
  <div class="pubteaser">
    <a href="{{pub.hlink}}">
    <img
      src="images/{{pub.id}}.png"
    />
    </a>
  </div>
  <div class="pubdata">
  <div class="pubtitle">{{ pub.title }}</div>
  <div class="pubauthors">{{ pub.authors }}</div>
  <div class="pubinfo">{{ pub.publication }}, {{ pub.year}}</div>
  <div class="publinks">
      <a href="pdfs/{{ pub.id}}.pdf"><i class="far fa-file-pdf"></i> PDF</a
      >&nbsp;&nbsp;
  </div>
  </div>

</div>
{% endfor %}
