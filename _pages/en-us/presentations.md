---
page_id: presentations
layout: page
permalink: /presentations/
title: presentations
description: Oral and poster presentations.
nav: true
nav_order: 3
tabs: true
---

<p style="font-size: 0.9em; margin-bottom: 0.5em;">
  Future dates represent scheduled events.
</p>
<p style="font-size: 0.9em; margin-bottom: 0.5em;">
  Japanese-language presentations are listed on the Japanese page only.
</p>
<p style="font-size: 0.9em; margin-bottom: 1em;">
  <u>Underline</u>: FEBQI lab member &nbsp;|&nbsp; <sup>*</sup>: Corresponding author/presenter
</p>

{% assign years = site.data.presentations | map: "year" | uniq | sort | reverse %}

<ul class="tab" data-tab="tab-presentations-en">
  {% for year in years %}
    <li{% if forloop.first %} class="active"{% endif %}><a href="#">{{ year }}</a></li>
  {% endfor %}
  <li><a href="#">Before 2023</a></li>
</ul>

<ul id="tab-presentations-en" class="tab-content">
{% for year in years %}
<li{% if forloop.first %} class="active"{% endif %}>
{% assign year_pres = site.data.presentations | where: "year", year %}
<table class="table table-sm" style="font-size: 0.9em;">
{% for pres in year_pres %}
  {% if pres.lang == "ja" %}{% continue %}{% endif %}
<tr>
  <td style="white-space: nowrap; padding-right: 1em; color: #888;">{{ pres.date }}</td>
  <td>
    <div>
      <strong>{{ pres.title }}</strong>
      {% if pres.type == "Oral" %}<span class="badge" style="background:#aaa; color:#fff; font-size:0.8em;">Oral</span>
      {% else %}<span class="badge" style="background:#aaa; color:#fff; font-size:0.8em;">Poster</span>{% endif %}
      {% if pres.invited %}&nbsp;<span class="badge" style="background:#888; color:#fff; font-size:0.8em;">Invited</span>{% endif %}
      {% if pres.reviewed %}&nbsp;<span class="badge" style="background:#555; color:#fff; font-size:0.8em;">Reviewed</span>{% endif %}
      {% if pres.lang == "ja" %}&nbsp;<span class="badge" style="background:#888; color:#fff; font-size:0.8em;">Japanese</span>{% endif %}
    </div>
    <div>{% if pres.presenter_en_html %}{{ pres.presenter_en_html }}{% else %}{{ pres.presenter_html }}{% endif %}</div>
    <div style="font-size:0.9em;"><em>{{ pres.conference }}</em>{% if pres.venue_en %}, {{ pres.venue_en }}{% elsif pres.venue %}, {{ pres.venue }}{% endif %}</div>
    <div class="links">
      {% if pres.url %}<a href="{{ pres.url }}" class="btn btn-sm z-depth-0" role="button">Link</a>{% endif %}
    </div>
  </td>
</tr>
{% endfor %}
</table>
</li>
{% endfor %}

<li>
<table class="table table-sm" style="font-size: 0.9em;">
{% for pres in site.data.presentations_old %}
  {% if pres.lang == "J" %}{% continue %}{% endif %}
<tr>
  <td style="white-space: nowrap; padding-right: 1em; color: #888;">{{ pres.date }}</td>
  <td>
    <div>
      <strong>{{ pres.title }}</strong>
      {% if pres.type == "Oral" %}<span class="btn btn-sm z-depth-0" style="background-color:#e8f4f8; color:#2a7ae2; cursor:default; font-size:0.75em; vertical-align:middle; padding:0.1em 0.35em; line-height:1.2;">Oral</span>
      {% else %}<span class="btn btn-sm z-depth-0" style="background-color:#f0f0f0; color:#555; cursor:default; font-size:0.75em; vertical-align:middle; padding:0.1em 0.35em; line-height:1.2;">Poster</span>{% endif %}
      {% if pres.invited %}<span class="btn btn-sm z-depth-0" style="background-color:#fff3e0; color:#e65100; cursor:default; font-size:0.75em; vertical-align:middle; padding:0.1em 0.35em; line-height:1.2;">Invited</span>{% endif %}
      {% if pres.reviewed %}<span class="btn btn-sm z-depth-0" style="background-color:#f1f8e9; color:#33691e; cursor:default; font-size:0.75em; vertical-align:middle; padding:0.1em 0.35em; line-height:1.2;">Reviewed</span>{% endif %}
    </div>
    <div>{{ pres.presenter_html }}</div>
    <div style="font-size:0.9em;"><em>{{ pres.conference }}</em>{% if pres.venue %}, {{ pres.venue }}{% endif %}</div>
    <div class="links">
      {% if pres.url %}<a href="{{ pres.url }}" class="btn btn-sm z-depth-0" role="button">Link</a>{% endif %}
    </div>
  </td>
</tr>
{% endfor %}
</table>
</li>

</ul>
