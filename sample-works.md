---
title: Sample works
mount: code_samples
mount: samples
navbar: true
---
## Writing samples

<ol>
{% for item in site.data.writingsampleconfig.toc %}
  <h3>{{item.title}}</h3>
  {% for entry in item.pages %}
  <li>
    <a href="{{ entry.link }}">{{ entry.page }}</a>
  </li>
  {% endfor %}
{% endfor %}
</ol>

## Code samples

<ul>
{% for item in site.data.codesampleconfig.toc %}
  <h3>{{item.title}}</h3>
  {% for entry in item.pages %}
  <li>
    <a href="{{ entry.link }}">{{ entry.page }}</a>
  </li>
  {% endfor %}
{% endfor %}
</ul>

## Doc sets I've worked on

* [Portworx (2.1 - Present)](https://docs.portworx.com)
* [Vertica (7.X)](https://www.vertica.com/documentation/vertica/)
* [Celtra (private documentation)](http://support.celtra.com)
* [Red Hat 3scale (SaaS, 2.0, 2.1, 2.2)](https://access.redhat.com/documentation/en-us/red_hat_3scale_api_management/2.2/)
