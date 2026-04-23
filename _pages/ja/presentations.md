---
page_id: presentations
layout: page
permalink: /presentations/
title: 発表
description: 口頭・ポスター発表一覧。
nav: true
nav_order: 3
tabs: true
---

<p style="font-size: 0.9em; margin-bottom: 0.5em;">
  未来の日付は予定されている発表を表します。
</p>
<p style="font-size: 0.9em; margin-bottom: 1em;">
  <u>下線</u>: FEBQIメンバー &nbsp;|&nbsp; <sup>*</sup>: 責任著者/発表者
</p>

{% assign years = site.data.presentations | map: "year" | uniq | sort | reverse %}

<ul class="tab" data-tab="tab-presentations-ja">
  {% for year in years %}
    <li{% if forloop.first %} class="active"{% endif %}><a href="#">{{ year }}</a></li>
  {% endfor %}
  <li><a href="#">〜2022年</a></li>
</ul>

<ul id="tab-presentations-ja" class="tab-content">
{% for year in years %}
<li{% if forloop.first %} class="active"{% endif %}>
{% assign year_pres = site.data.presentations | where: "year", year %}
<table class="table table-sm" style="font-size: 0.9em;">
{% for pres in year_pres %}
<tr>
  <td style="white-space: nowrap; padding-right: 1em; color: #888;">{{ pres.date }}</td>
  <td>
    <div>
      <strong>{{ pres.title }}</strong>
      {% if pres.type == "Oral" %}<span class="btn btn-sm z-depth-0" style="background-color:#e8f4f8; color:#2a7ae2; cursor:default; font-size:0.75em; vertical-align:middle;">口頭</span>
      {% else %}<span class="btn btn-sm z-depth-0" style="background-color:#f0f0f0; color:#555; cursor:default; font-size:0.75em; vertical-align:middle;">ポスター</span>{% endif %}
      {% if pres.invited %}<span class="btn btn-sm z-depth-0" style="background-color:#fff3e0; color:#e65100; cursor:default; font-size:0.75em; vertical-align:middle;">招待</span>{% endif %}
      {% if pres.reviewed %}<span class="btn btn-sm z-depth-0" style="background-color:#f1f8e9; color:#33691e; cursor:default; font-size:0.75em; vertical-align:middle;">審査あり</span>{% endif %}
      {% if pres.lang == "en" %}<span class="btn btn-sm z-depth-0" style="background-color:#e8eaf6; color:#283593; cursor:default; font-size:0.75em; vertical-align:middle;">英語</span>{% endif %}
    </div>
    <div>{{ pres.presenter_html }}</div>
    <div style="font-size:0.9em;"><em>{{ pres.conference }}</em>{% if pres.venue %}, {{ pres.venue }}{% endif %}</div>
    <div class="links">
      {% if pres.url %}<a href="{{ pres.url }}" class="btn btn-sm z-depth-0" role="button">リンク</a>{% endif %}
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
<tr>
  <td style="white-space: nowrap; padding-right: 1em; color: #888;">{{ pres.date }}</td>
  <td>
    <div>
      <strong>{{ pres.title }}</strong>
      {% if pres.type == "Oral" %}<span class="btn btn-sm z-depth-0" style="background-color:#e8f4f8; color:#2a7ae2; cursor:default; font-size:0.75em; vertical-align:middle;">口頭</span>
      {% else %}<span class="btn btn-sm z-depth-0" style="background-color:#f0f0f0; color:#555; cursor:default; font-size:0.75em; vertical-align:middle;">ポスター</span>{% endif %}
      {% if pres.invited %}<span class="btn btn-sm z-depth-0" style="background-color:#fff3e0; color:#e65100; cursor:default; font-size:0.75em; vertical-align:middle;">招待</span>{% endif %}
      {% if pres.reviewed %}<span class="btn btn-sm z-depth-0" style="background-color:#f1f8e9; color:#33691e; cursor:default; font-size:0.75em; vertical-align:middle;">審査あり</span>{% endif %}
    </div>
    <div>{{ pres.presenter_html }}</div>
    <div style="font-size:0.9em;"><em>{{ pres.conference }}</em>{% if pres.venue %}, {{ pres.venue }}{% endif %}</div>
    <div class="links">
      {% if pres.url %}<a href="{{ pres.url }}" class="btn btn-sm z-depth-0" role="button">リンク</a>{% endif %}
    </div>
  </td>
</tr>
{% endfor %}
</table>
</li>

</ul>
