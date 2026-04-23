---
page_id: outreach
layout: page
permalink: /outreach/
title: outreach
description: Review & tutorial articles, public lectures, and more
nav: true
nav_order: 7
---

## Review / Tutorial Articles

<p style="font-size: 0.9em; margin-bottom: 1em;">
  <u>Underline</u>: FEBQI lab member &nbsp;|&nbsp; <sup>*</sup>: Corresponding author
</p>

<table class="table table-sm" style="font-size: 0.9em;">
{% for article in site.data.tutorial_articles %}
<tr>
  <td style="white-space: nowrap; padding-right: 1em; color: #888;">{{ article.year }}</td>
  <td>
    <span class="author">{{ article.authors_html }}</span><br>
    {{ article.title }}<br>
    <em>{{ article.journal }}</em><br>
    &nbsp;<span class="badge" style="background:#aaa; color:#fff; font-size:0.8em;">{{ article.lang }}</span>
    {% if article.invited %}&nbsp;<span class="badge" style="background:#888; color:#fff; font-size:0.8em;">Invited</span>{% endif %}
    {% if article.reviewed %}&nbsp;<span class="badge" style="background:#555; color:#fff; font-size:0.8em;">Reviewed</span>{% endif %}
    <div class="links">
      {% if article.journal_url %}<a href="{{ article.journal_url }}" class="btn btn-sm z-depth-0" role="button" target="_blank">Journal</a>{% endif %}
      {% if article.draft_url %}<a href="{{ article.draft_url }}" class="btn btn-sm z-depth-0" role="button" target="_blank">Draft</a>{% endif %}
    </div>
  </td>
</tr>
{% endfor %}
</table>

## Outreach Activities & Seminars

<p style="font-size: 0.9em; margin-bottom: 1em;">
  <u>Underline</u>: FEBQI lab member
</p>

<table class="table table-sm" style="font-size: 0.9em;">
{% for act in site.data.outreach_activities %}
<tr>
  <td style="white-space: nowrap; padding-right: 1em; color: #888;">{{ act.date }}</td>
  <td>
    {% if act.presenter_en_html %}{{ act.presenter_en_html }}{% else %}{{ act.presenter_html }}{% endif %}<br>
    {{ act.title }}<br>
    <em>{% if act.venue_en %}{{ act.venue_en }}{% else %}{{ act.venue }}{% endif %}</em>
    <div class="links">
      <span class="btn btn-sm z-depth-0" style="background-color:#f0f0f0; color:#555; cursor:default;">{{ act.format }}</span>
      {% if act.url %}<a href="{{ act.url }}" class="btn btn-sm z-depth-0" role="button" target="_blank">Link</a>{% endif %}
    </div>
  </td>
</tr>
{% endfor %}
</table>

<details>
<summary style="color:#999; font-size:0.9em; cursor:pointer; margin-top:1.5rem;">― Before 2023 ―</summary>
<table class="table table-sm" style="font-size: 0.9em; margin-top:0.5rem;">
{% for act in site.data.outreach_activities_old %}
<tr>
  <td style="white-space: nowrap; padding-right: 1em; color: #888;">{{ act.date }}</td>
  <td>
    {{ act.presenter_html }}<br>
    {{ act.title }}<br>
    <em>{{ act.venue }}</em>
    <div class="links">
      <span class="btn btn-sm z-depth-0" style="background-color:#f0f0f0; color:#555; cursor:default;">{{ act.format }}</span>
      {% if act.url %}<a href="{{ act.url }}" class="btn btn-sm z-depth-0" role="button" target="_blank">Link</a>{% endif %}
    </div>
  </td>
</tr>
{% endfor %}
</table>
</details>
