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
    <br>
    {% if article.journal_url %}<a href="{{ article.journal_url }}" class="btn btn-sm z-depth-0" role="button" target="_blank">Journal</a>{% endif %}
    {% if article.draft_url %}<a href="{{ article.draft_url }}" class="btn btn-sm z-depth-0" role="button" target="_blank">Draft</a>{% endif %}
  </td>
</tr>
{% endfor %}
</table>
