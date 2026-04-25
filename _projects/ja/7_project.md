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

<p style="margin-bottom:0.2rem"><strong>使用技術：</strong></p>
<ul style="margin-top:0.2rem">
  <li><a href="https://jekyllrb.com/">Jekyll</a>（静的サイトジェネレーター）</li>
  <li><a href="https://github.com/alshedivat/al-folio">al-folio</a> テーマ（<a href="https://github.com/george-gca/multi-language-al-folio">多言語対応fork</a> 使用）</li>
  <li><a href="https://github.com/untra/polyglot">jekyll-polyglot</a>（日英バイリンガル対応）</li>
  <li><a href="https://github.com/inukshuk/jekyll-scholar">jekyll-scholar</a>（BibTeX論文リスト）</li>
  <li><a href="https://pages.github.com/">GitHub Pages</a>（ホスティング）</li>
</ul>

<p style="margin-bottom:0.2rem"><strong>主な機能：</strong></p>
<ul style="margin-top:0.2rem">
  <li>レスポンシブデザイン・ダーク/ライトモード対応</li>
  <li>トップページにサムネイル付きブログカード表示（新記事追加で自動更新）</li>
</ul>

<p style="margin-bottom:0.2rem"><strong>ローカルでの確認：</strong></p>
<p style="margin-top:0.2rem">GitHub Pagesのビルドには数分かかりますが、ローカルで <a href="https://jekyllrb.com/docs/usage/">jekyll serve</a> を使えば変更を即座に確認できます。ファイルを保存するたびに自動リビルドされるため、GitHubにpushせずにリアルタイムでプレビューできます。</p>

<p style="margin-bottom:0.2rem"><strong>モバイルからの更新：</strong></p>
<p style="margin-top:0.2rem"><a href="https://decapcms.org/">Decap CMS</a> を導入しており、スマートフォンのブラウザから <code>/admin</code> にアクセスするだけでブログ記事の投稿・編集ができます。Markdownを直接書く必要はなく、フォーム形式で入力してGitHubにpushするところまで自動で行われます。</p>

<p style="margin-bottom:0.2rem"><strong>ソースコード：</strong></p>
<p style="margin-top:0.2rem">全ソースコードは <a href="https://github.com/febqi/lab-hp">GitHubで公開</a> しています。</p>
