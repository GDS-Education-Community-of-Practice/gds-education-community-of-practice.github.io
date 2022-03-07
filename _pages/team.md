---
title: "DSECOP - Team"
layout: gridlay
excerpt: "DSECOP: Team members"
sitemap: false
permalink: /team/
---

# Principal Investigators
{% assign number_printed = 0 %}
{% for member in site.data.pis %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="33%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} </i>
  <br>Email: <{{ member.email }}>
  <br>Web: <{{ member.website }}>
  <br>Affiliation: {{ member.aff }}
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


# Fellows
{% assign number_printed = 0 %}
{% for member in site.data.fellows %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <!-- <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="33%" style="float: left" /> -->
  <h4>{{ member.name }}</h4>
  <!-- <i>{{ member.info }} </i>
  <br>Email: <{{ member.email }}>
  <br>Web: <{{ member.website }}>
  <br>Affiliation: {{ member.aff }} -->
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

# Community Manager
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/zenginoglu.jpg" class="img-responsive" width="33%" style="float: left" />
  <h4>Anıl Zenginoğlu</h4>
  <i> Works on wave equations, black holes, gravitational waves, and null infinity.</i>
  <br>Email: <a href="mailto:anil@umd.edu">anil@umd.edu</a>
  <br>Web: <a href="https://anilzen.github.io">anilzen.github.io</a>
  <br>Affiliation: IPST at the University of Maryland
</div>
