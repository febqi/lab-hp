---
page_id: presentations
layout: page
permalink: /presentations/
title: presentations
description: Oral and poster presentations.
nav: true
nav_order: 3
---

<p style="font-size: 0.9em; margin-bottom: 0.5em;">
  Future dates represent scheduled events.
</p>
<p style="font-size: 0.9em; margin-bottom: 1.5em;">
  <u>Underline</u>: FEBQI lab member &nbsp;|&nbsp; <sup>*</sup>: Corresponding author/presenter
</p>

{% assign sorted_presentations = site.data.presentations | sort: "year" | reverse %}
{% assign current_year = 0 %}

{% for pres in sorted_presentations %}
  {% if pres.year != current_year %}
    {% assign current_year = pres.year %}
<h2>{{ current_year }}</h2>
  {% endif %}

<div class="publication-item" style="margin-bottom: 1em;">
  <div>
    <strong>{{ pres.title }}</strong>
  </div>
  <div>
    {% if pres.presenter_en_html %}
      {{ pres.presenter_en_html }}
    {% else %}
      {{ pres.presenter_html }}
    {% endif %}
  </div>
  <div class="periodical" style="font-size: 0.9em;">
    <em>{{ pres.conference }}</em>{% if pres.venue_en %}, {{ pres.venue_en }}{% elsif pres.venue %}, {{ pres.venue }}{% endif %} ({{ pres.date }})
  </div>
  <div class="links">
    {% if pres.type == "Oral" %}
      <span class="btn btn-sm z-depth-0" style="background-color:#e8f4f8; color:#2a7ae2; cursor:default;">Oral</span>
    {% else %}
      <span class="btn btn-sm z-depth-0" style="background-color:#f0f0f0; color:#555; cursor:default;">Poster</span>
    {% endif %}
    {% if pres.invited %}
      <span class="btn btn-sm z-depth-0" style="background-color:#fff3e0; color:#e65100; cursor:default;">Invited</span>
    {% endif %}
    {% if pres.reviewed %}
      <span class="btn btn-sm z-depth-0" style="background-color:#f1f8e9; color:#33691e; cursor:default;">Reviewed</span>
    {% endif %}
    {% if pres.lang == "ja" %}
      <span class="btn btn-sm z-depth-0" style="background-color:#fce4ec; color:#880e4f; cursor:default;">Japanese</span>
    {% endif %}
    {% if pres.url %}
      <a href="{{ pres.url }}" class="btn btn-sm z-depth-0" role="button">Link</a>
    {% endif %}
  </div>
</div>

{% endfor %}
