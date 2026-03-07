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
  <br>Web: <a href="{{ member.website }}">{{ member.website | remove: "https://" }}</a>
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
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/soltanieh-ha.jpg" class="img-responsive" width="33%" style="float: left" />
  <h4>Mohammad Soltaniehha</h4>
  <i>Computational condensed matter physics, machine learning in cancer research and forecasting, and embodied AI. Co-founder of GDS (APS's Data Science Unit).</i>
  <br>Email: <a href="mailto:msoltani@bu.edu">msoltani@bu.edu</a>
  <br>Web: <a href="https://soltaniehha.com">soltaniehha.com</a>
  <br>Affiliation: Boston University
</div>
</div>

# 2026 Fellows

We are accepting applications for the 2026 DSECOP Fellowship cohort. [View the full announcement and apply here.]({{ site.url }}{{ site.baseurl }}/fellowship/)

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
  <br> Web: {% if member.website %} <{{ member.website }}> {% else %} <a href="{{ site.url }}{{ site.baseurl }}/team/">DSECOP Fellows</a> {% endif %}
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
  <br> Web: {% if member.website %} <{{ member.website }}> {% else %} <a href="{{ site.url }}{{ site.baseurl }}/team/">DSECOP Fellows</a> {% endif %}
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

# Former Project Contributors

We gratefully acknowledge the contributions of the following individuals to DSECOP:

- **Wolfgang Losert** — Principal Investigator, IPST and Physics at the University of Maryland
- **Maria (Marilena) Longobardi** — Principal Investigator, University of Basel
- **Jacob Hale** — Reviewer, DePauw University
- **Anıl Zenginoğlu** — Community Manager, IPST at the University of Maryland
