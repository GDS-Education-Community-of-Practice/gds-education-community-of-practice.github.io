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

# Editor-in-Chief

<div class="row">

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/soltanieh-ha.jpg" class="img-responsive" width="36%" style="float: left" />
  <h4>Mohammad Soltanieh-ha</h4>
  <i> Strongly correlated electronic systems in low dimensions, computer vision in cancer diagnosis, high-performance computing. Faculty Expert at Google Cloud.</i>
  <br>Email: <a href="mailto:msoltani@bu.edu">msoltani@bu.edu</a>
  <br>Web: <a href="https://www.bu.edu/questrom/profile/mohammad-soltanieh-ha/">https://www.bu.edu/questrom/profile/mohammad-soltanieh-ha/</a>
  <br>Affiliation: Questrom School of Business at Boston University
</div>
</div>

# Reviewer

<div class="row">

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/hale.jpg" class="img-responsive" width="36%" style="float: left" />
  <h4>Jacob Hale</h4>
  <i> Applying physical laws and theories to understand how viruses pack DNA, how bacteria respond to osmotic shock, and how membrane proteins in human cancer cells function.</i>
  <br>Email: <a href="mailto:jacobhale@depauw.edu">jacobhale@depauw.edu</a>
  <br>Web: <a href="https://www.depauw.edu/academics/departments-programs/physics-astronomy/faculty-staff/faculty-staff-websites/j-hale/">https://www.depauw.edu/academics/departments-programs/physics-astronomy/faculty-staff/faculty-staff-websites/j-hale/</a>
  <br>Affiliation: DePauw University
</div>
</div>

# 2023 Fellows

{% assign number_printed = 0 %}
{% for member in site.data.fellows_2023 %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="33%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} </i>
  <br>Email: <{{ member.email }}>
  <br> Web: {% if member.website %} <{{ member.website }}> {% else %} <a href="{{ site.url }}{{ site.baseurl }}/team#fellows">DSECOP Fellows</a> {% endif %}
  <br>Title: {{ member.title }}
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

# 2022 Fellows

{% assign number_printed = 0 %}
{% for member in site.data.fellows %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="33%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} </i>
  <br>Email: <{{ member.email }}>
  <br> Web: {% if member.website %} <{{ member.website }}> {% else %} <a href="{{ site.url }}{{ site.baseurl }}/team#fellows">DSECOP Fellows</a> {% endif %}
  <br>Title: {{ member.title }}
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

# Community Manager
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/zenginoglu.jpg" class="img-responsive" width="36%" style="float: left" />
  <h4>Anıl Zenginoğlu</h4>
  <i> Black holes, gravitational waves, hyperbolic geometry, and null infinity.</i>
  <br>Email: <a href="mailto:anil@umd.edu">anil@umd.edu</a>
  <br>Web: <a href="https://anilzen.github.io">anilzen.github.io</a>
  <br>Affiliation: IPST at the University of Maryland
</div>
