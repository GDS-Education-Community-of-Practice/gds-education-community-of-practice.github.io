---
title: "DSECOP - Webinars"
layout: gridlay
excerpt: "DSECOP: Webinars"
sitemap: false
permalink: /webinars/
---

## Data science in physics courses at undergraduate-focused departments (May 25, 2022) <a name="webinar"></a>

Curious what data science and physics looks like when the physics department primarily serves undergraduates? This webinar is for you! Our presenters will discuss how they have included data science in their undergraduate physics courses, providing examples of what they do and sharing lessons learned. We will have plenty of time for questions and discussion.

Please register to attend [here](https://umd.zoom.us/meeting/register/tJMtcuuupzwjG9cdXAuqNSgrpqPkFyrpLy5u).

The webinar will take place on Wednesday, May 25th, at 1:00 pm. The moderator is the PI of the program, [William Ratcliff](https://www.nist.gov/people/william-d-ratcliff). The panelists are [Matthew Bellis](https://www.siena.edu/faculty-and-staff/person/matthew-bellis/) from Siena College and [Amy Roberts](https://clas.ucdenver.edu/physics/amy-roberts-phd) from UC Denver. 

<div class="row">

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>Matthew Bellis</pubtit>
  <img src="/images/eventpic/bellis.jpg" class="img-responsive" width="33%" style="float: left" />
  <p>Matt Bellis is an Associate Professor in Siena College's Department of Physics and Astronomy and the coordinator for Siena's Data Science program. He received his PhD from Rensselaer and came to Siena in 2012 after research associate positions at Carnegie Mellon, Stanford, and Northern Illinois University. He has conducted primarily particle physics research with the CLAS and GlueX experiments at Jefferson Lab, BaBar at SLAC, and now with the CMS experiment at the LHC. He is passionate about education and outreach and how data science can be leveraged for social good. He has engaged with students on sports analytics, mathematics and machine learning, and has a long-standing collaboration with other faculty and community groups exploring the allocation of resources to support homeless individuals and families. 
</p>
 </div>
</div>

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>Amy Roberts</pubtit>
  <img src="/images/eventpic/roberts.jpg" class="img-responsive" width="33%" style="float: left" />
  <!-- <p>Amy Roberts</p> -->
 </div>
</div>

</div>

<p> &nbsp; </p>

## Teaching data science to physicists (March 4, 2022) <a name="webinar"></a>

Webinar on Friday, March 4th, at 10:30 am to discuss teaching data science to physicists and material scientists. In this hour-long webinar, the panelists presented strategies and challenges of incorporating data science into physics curricula for students and researchers from all backgrounds. They provided guidance on how to best implement data science and machine learning in physics teaching and research.

You can watch a recording of the webinar below.

<iframe width="560" height="315" src="https://www.youtube.com/embed/TNLaVmLV6mw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

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