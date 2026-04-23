---
page_id: project_7
layout: page
title: このウェブサイト
description: JekyllとGitHub Pagesで構築、主にClaude Codeが作成
img: assets/img/team_pic.png
importance: 1
category: fun
---

このウェブサイトは [Jekyll](https://jekyllrb.com/) で構築され、[GitHub Pages](https://pages.github.com/) でホスティングされています。テーマは [al-folio](https://github.com/alshedivat/al-folio) を使用し、多言語対応は [jekyll-polyglot](https://github.com/untra/polyglot) で実現しています。

サイトの構築はウェブ担当者が日本語または英語で指示を出し、[Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview)（AnthropicのAIコーディングアシスタント）が全てのコードを書き、日英の翻訳も担当し、GitHubへのpushまで行いました。レイアウトのカスタマイズやCSSの修正から、新規ページの追加、文献管理、ブログ記事の作成まで、Claude Codeが担当しています。同じようなサイトを作りたい方は、まずソースコードをgitでローカルにクローンし、あとはClaude Codeに指示を出すだけ — ファイルの編集からGitHubへのpushまで全てやってくれます。日常的なメンテナンスも同様で、例えば新しい論文を追加するときは、ジャーナルページのURLをClaude Codeに渡すだけで、BibTeXの更新からpushまで全て対応してくれます。

**使用技術：**

- [Jekyll](https://jekyllrb.com/)（静的サイトジェネレーター）
- [al-folio](https://github.com/alshedivat/al-folio) テーマ（[多言語対応fork](https://github.com/george-gca/multi-language-al-folio) 使用）
- [jekyll-polyglot](https://github.com/untra/polyglot)（日英バイリンガル対応）
- [jekyll-scholar](https://github.com/inukshuk/jekyll-scholar)（BibTeX論文リスト）
- [GitHub Pages](https://pages.github.com/)（ホスティング）
- 写真：[Unsplash](https://unsplash.com/)

**主な機能：**

- レスポンシブデザイン・ダーク/ライトモード対応
- トップページにサムネイル付きブログカード表示（新記事追加で自動更新）

**ソースコード：**

全ソースコードは公開しています — [リポジトリ]({{ '/repositories/' | relative_url }}) ページへ。
