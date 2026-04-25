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

**Tech stack:**

- [Jekyll](https://jekyllrb.com/) static site generator
- [al-folio](https://github.com/alshedivat/al-folio) theme with [multi-language](https://github.com/george-gca/multi-language-al-folio) fork
- [jekyll-polyglot](https://github.com/untra/polyglot) for English/Japanese bilingual support
- [jekyll-scholar](https://github.com/inukshuk/jekyll-scholar) for BibTeX-based publication lists
- [GitHub Pages](https://pages.github.com/) for hosting

**Key features:**

- Responsive design with dark/light mode
- Top page automatically shows the 3 latest blog posts with thumbnail cards

**Source code:**

The full source code is publicly available — see the [Repositories]({{ '/repositories/' | relative_url }}) page.

**Local preview:**

GitHub Pages builds take a few minutes, but you can preview changes instantly using [jekyll serve](https://jekyllrb.com/docs/usage/) locally. Files are rebuilt automatically on save, so you can check edits in real time without pushing to GitHub.
