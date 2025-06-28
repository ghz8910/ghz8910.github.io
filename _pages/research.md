---
title: "Research"
layout: gridlay
sitemap: false
permalink: /research/
---

<style>
img{
  border-radius: 10px;
}
.col-md-3 {
  margin-top:10px;
  margin-bottom:10px;
  padding:0px;
  display:block;
  overflow:hidden;
  text-align:center;
  display: table-cell;
  background: white;
  border-radius: 20px;
  height: auto;
}
iframe {
  margin:0;
  padding:0;
  width: 175px;
  display: inline;
  vertical-align: middle;
}

</style>


<div class="jumbotron">
  <h4>Sponsors</h4>
  <div style='display:block; text-align:center; margin-left:auto; margin-right:auto;'>
  {% for funder in site.data.funders %}<a href="{{ funder.url }}" target="_blank"><img src='{{ site.url }}{{ site.baseurl }}/images/{{ funder.image }}' style='max-height: 80px; max-width: 200px; margin: 1%'/></a>{% endfor %}
  </div>
</div>

#### Research Projects

<div class='jumbotron'>
{% assign number_printed = 0 %}
{% for project in site.data.projects %}
<div class="row">

<div class="col-sm-6">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ project.image }}" width="100%" style="max-width:450px"/>
</div>
<div class="col-sm-6 col-xs-12">
  <h4>{{ project.title }}</h4>
  <i>{{ project.description }}<br></i>
  <i>Sponsor: {{ project.sponsor}}<br></i>
{% if project.website %}<a href="{{ project.website }}" target="_blank"><i class="fa fa-home fa-2x"></i></a> {% endif %}

</div>
<!-- </div> -->

</div>
{% endfor %}
</div>