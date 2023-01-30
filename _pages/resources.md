---
title: "DSECOP - Resources"
layout: textlay
excerpt: "DSECOP funded by APS"
sitemap: false
permalink: /resources
---
## Resources for Involvement

We aim to build a community of researchers, practitioners, and learners to engage with the teaching and education of data science. There are multiple ways to get involved in the conversation.

- Join our [Slack Channel](https://join.slack.com/t/aps-gds/shared_invite/zt-cc04p8jl-DQ~a~DMn8_iHBnjaBSL_6A)
- Subscribe to the [DSECOP newsletter](https://dsecop.substack.com/)
- Email us at <dsecop@aps.org>

{::nomarkdown}
<div>
    {% assign sm = site.data.social %}
    {% for entry in sm %}
        {% assign key = entry | first %}
        {% if sm[key].id %}
            <a href="{{ sm[key].href }}{{ sm[key].id }}" title="{{ sm[key].title }}">
            <i class="fa {{ sm[key].fa-icon}}" style="font-size: 3em;"></i></a>
        {% endif %}
    {% endfor %}
<div>
{:/}

## Resources on Learning Python
- [A Whirlwind Tour of Python](https://jakevdp.github.io/WhirlwindTourOfPython/) by [Jake VanderPlas](http://vanderplas.com/).
- [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/) by [Jake VanderPlas](http://vanderplas.com/).
- [Plotting and Programming in Python](http://swcarpentry.github.io/python-novice-gapminder/) from [Software Carpentry](https://software-carpentry.org/).


## Resources on Data Science Education

- [Edison Data Science Framework](https://edison-project.eu/edison/edison-data-science-framework-edsf/) 

<img src="{{ site.url }}{{ site.baseurl }}/images/resources/Slack_QR.png" class="img-responsive" width="18%" style="float: left" />
<img src="{{ site.url }}{{ site.baseurl }}/images/resources/Social.png" class="img-responsive" width="32%" style="float: left" />