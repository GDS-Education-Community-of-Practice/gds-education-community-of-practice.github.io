---
title: "DSECOP - Events"
layout: gridlay
excerpt: "DSECOP: Events"
sitemap: false
permalink: /events/
---

## Teaching Data Science to Physicists (March 4, 2022) <a name="webinar"></a>

Webinar on Friday, March 4th, at 10:30 am to discuss teaching data science to physicists and material scientists. In this hour-long webinar, the panelists presented strategies and challenges of incorporating data science into physics curricula for students and researchers from all backgrounds. They provided guidance on how to best implement data science and machine learning in physics teaching and research.

The webinar was moderated by the PI of the program, [William Ratcliff](https://www.nist.gov/people/william-d-ratcliff). The panelists were [Boris Kozinsky](https://bkoz.seas.harvard.edu/people/boris-kozinsky) from the Harvard School of Engineering and Applied Sciences, [Aaron Gilad Kusne](https://www.nist.gov/people/aaron-gilad-kusne) from the National Institute of Standards and Technology, [Federica Bianco](http://fbb.space/) from the University of Delaware, [Trevor David Rhone](https://science.rpi.edu/physics/faculty/trevor-rhone) from the Rensselaer Polytechnic Institute, and [Mohammad Soltanieh-Ha](https://www.bu.edu/questrom/profile/mohammad-soltanieh-ha/) from Boston University.

{% assign number_printed = 0 %}
{% for speaker in site.data.speakers %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ speaker.name }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/eventpic/{{ speaker.photo }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ speaker.bio }}</p>
 </div>
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

<p> &nbsp; </p>