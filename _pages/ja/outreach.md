---
page_id: outreach
layout: page
permalink: /outreach/
title: アウトリーチ
description: 解説記事・一般向け講演など
nav: true
nav_order: 7
---

## 解説記事

<p style="font-size: 0.9em; margin-bottom: 1em;">
  <u>下線</u>: FEBQI研究室メンバー &nbsp;|&nbsp; <sup>*</sup>: 責任著者（Corresponding author）
</p>

<table class="table table-sm" style="font-size: 0.9em;">
{% for article in site.data.tutorial_articles %}
<tr>
  <td style="white-space: nowrap; padding-right: 1em; color: #888;">{{ article.year }}</td>
  <td>
    {% if article.authors_ja_html %}{{ article.authors_ja_html }}{% else %}{{ article.authors_html }}{% endif %}<br>
    {% if article.journal_url %}<a href="{{ article.journal_url }}" target="_blank">{{ article.title }}</a>{% else %}{{ article.title }}{% endif %}<br>
    <em>{{ article.journal }}</em>
    &nbsp;<span class="badge" style="background:#aaa; color:#fff; font-size:0.8em;">{{ article.lang }}</span>
    {% if article.invited %}&nbsp;<span class="badge" style="background:#888; color:#fff; font-size:0.8em;">招待</span>{% endif %}
    {% if article.reviewed %}&nbsp;<span class="badge" style="background:#555; color:#fff; font-size:0.8em;">査読あり</span>{% endif %}
  </td>
</tr>
{% endfor %}
</table>
