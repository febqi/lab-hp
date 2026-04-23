---
page_id: presentations
layout: page
permalink: /presentations/
title: 発表
description: 口頭・ポスター発表一覧。
nav: true
nav_order: 3
---

<p style="font-size: 0.9em; margin-bottom: 0.5em;">
  未来の日付は予定されている発表を表します。
</p>
<p style="font-size: 0.9em; margin-bottom: 1.5em;">
  <u>下線</u>: FEBQIメンバー &nbsp;|&nbsp; <sup>*</sup>: 責任著者/発表者
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
    {% if pres.invited %}
      <span class="btn btn-sm z-depth-0" style="background-color:#fff3e0; color:#e65100; cursor:default; font-size:0.75em; vertical-align:middle;">招待</span>
    {% endif %}
    {% if pres.reviewed %}
      <span class="btn btn-sm z-depth-0" style="background-color:#f1f8e9; color:#33691e; cursor:default; font-size:0.75em; vertical-align:middle;">審査あり</span>
    {% endif %}
  </div>
  <div>
    {{ pres.presenter_html }}
  </div>
  <div class="periodical" style="font-size: 0.9em;">
    <em>{{ pres.conference }}</em>{% if pres.venue %}, {{ pres.venue }}{% endif %} ({{ pres.date }})
  </div>
  <div class="links">
    {% if pres.type == "Oral" %}
      <span class="btn btn-sm z-depth-0" style="background-color:#e8f4f8; color:#2a7ae2; cursor:default;">口頭</span>
    {% else %}
      <span class="btn btn-sm z-depth-0" style="background-color:#f0f0f0; color:#555; cursor:default;">ポスター</span>
    {% endif %}
    {% if pres.lang == "en" %}
      <span class="btn btn-sm z-depth-0" style="background-color:#e8eaf6; color:#283593; cursor:default;">英語</span>
    {% endif %}
    {% if pres.url %}
      <a href="{{ pres.url }}" class="btn btn-sm z-depth-0" role="button">リンク</a>
    {% endif %}
  </div>
</div>

{% endfor %}

<details>
<summary style="color:#999; font-size:0.9em; cursor:pointer; margin-top:1.5rem;">― 2023年以前 ―</summary>
{% for pres in site.data.presentations_old %}
<div style="margin-bottom:0.8rem; padding-top:0.5rem; border-top:1px solid var(--global-divider-color);">
  <span style="font-size:0.85em; color:#888;">{{ pres.date }}</span>
  &nbsp;<span class="btn btn-sm z-depth-0" style="background-color:#eee; color:#555; cursor:default; font-size:0.75em;">{{ pres.type }}</span>
  <div>{{ pres.presenter_html }}<br>{{ pres.title }}<br><em>{{ pres.conference }}</em>{% if pres.venue %}, {{ pres.venue }}{% endif %}</div>
  <div class="links">
    {% if pres.invited %}<span class="btn btn-sm z-depth-0" style="background-color:#fff3e0; color:#e65100; cursor:default;">招待</span>{% endif %}
    {% if pres.reviewed %}<span class="btn btn-sm z-depth-0" style="background-color:#f1f8e9; color:#33691e; cursor:default;">審査あり</span>{% endif %}
    {% if pres.url %}<a href="{{ pres.url }}" class="btn btn-sm z-depth-0" role="button">リンク</a>{% endif %}
  </div>
</div>
{% endfor %}
</details>
