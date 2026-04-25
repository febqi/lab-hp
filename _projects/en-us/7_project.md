---
page_id: project_7
layout: page
title: This Website
description: Built with Jekyll and GitHub Pages, primarily by Claude Code
img: assets/img/team_pic.png
importance: 1
category: fun
---

This lab website is built with [Jekyll](https://jekyllrb.com/) and hosted on [GitHub Pages](https://pages.github.com/), using the [al-folio](https://github.com/alshedivat/al-folio) theme with multilingual support via [jekyll-polyglot](https://github.com/untra/polyglot).

The site was built through conversations with [Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview) (Anthropic's AI coding assistant) — the person in charge provided instructions in English or Japanese, and Claude Code wrote all the code, handled translations between the two languages, and pushed changes to GitHub. Claude Code handled everything from layout customization and CSS fixes to adding new pages, bibliography management, and blog posts. If you'd like to build something similar: clone the source code locally with git, then let Claude Code do the rest — editing files and pushing changes to GitHub. Day-to-day maintenance works the same way: for example, adding a new publication just requires sharing the journal page URL with Claude Code, and it handles everything from updating the BibTeX to pushing the changes.

<p style="margin-bottom:0.2rem"><strong>Tech stack:</strong></p>
<ul style="margin-top:0.2rem">
  <li><a href="https://jekyllrb.com/">Jekyll</a> static site generator</li>
  <li><a href="https://github.com/alshedivat/al-folio">al-folio</a> theme with <a href="https://github.com/george-gca/multi-language-al-folio">multi-language</a> fork</li>
  <li><a href="https://github.com/untra/polyglot">jekyll-polyglot</a> for English/Japanese bilingual support</li>
  <li><a href="https://github.com/inukshuk/jekyll-scholar">jekyll-scholar</a> for BibTeX-based publication lists</li>
  <li><a href="https://pages.github.com/">GitHub Pages</a> for hosting</li>
</ul>

<p style="margin-bottom:0.2rem"><strong>Key features:</strong></p>
<ul style="margin-top:0.2rem">
  <li>Responsive design with dark/light mode</li>
  <li>Top page automatically shows the 3 latest blog posts with thumbnail cards</li>
</ul>

<p style="margin-bottom:0.2rem"><strong>Local preview:</strong></p>
<p style="margin-top:0.2rem">GitHub Pages builds take a few minutes, but you can preview changes instantly using <a href="https://jekyllrb.com/docs/usage/">jekyll serve</a> locally. Files are rebuilt automatically on save, so you can check edits in real time without pushing to GitHub.</p>

<p style="margin-bottom:0.2rem"><strong>Mobile editing:</strong></p>
<p style="margin-top:0.2rem">The site includes <a href="https://decapcms.org/">Decap CMS</a>, so blog posts can be created and edited directly from a smartphone browser via <code>/admin</code> — no need to write Markdown manually. Changes are committed and pushed to GitHub automatically.</p>

<p style="margin-bottom:0.2rem"><strong>Source code:</strong></p>
<p style="margin-top:0.2rem">The full source code is <a href="https://github.com/febqi/lab-hp">publicly available on GitHub</a>.</p>
