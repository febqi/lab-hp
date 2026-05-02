---
page_id: project_1
layout: page
title: 液体ヘリウム上の電子
description: 清浄な環境でのスケーラブルな電子スピン量子ビット
img: assets/img/helium_plasmon-06.png
importance: 1
category: research
related_publications: true
---

<div class="alert alert-warning" role="alert" style="font-size:0.9em;">
  🚧 このページは現在作成中です。
</div>

液体ヘリウム上の電子は、不純物や格子欠陥の影響を受けない、極めてクリーンな量子コンピューティングプラットフォームである。中でもスピン状態は、他の系と比べて非常に長いコヒーレンス時間を持つと理論的に予測されており、量子ビットとしての利用が注目されている。一方で、スピン状態の読み出しは依然として困難である。そこで我々は、スピン状態をリュードベリ状態にマッピングし、LC回路を用いてその遷移を高感度に検出する手法を提案・実証した。周波数変調を加えたマイクロ波によりリュードベリ準位の遷移を誘起し、量子キャパシタンスの変化として読み出すことで、単一電子のリュードベリ遷移を識別できる感度を実現した。この成果は、スケーラブルなスピン読み出しへの道を開くものである。

<img src="{{ '/assets/img/rydberg_rf.png' | relative_url }}" class="img-fluid rounded z-depth-1" style="width:70%; display:block; margin:0 auto;">
<p style="font-size:0.85em; color:#888; text-align:center; margin-top:0.5rem;">マイクロ波（MW）キャリア周波数 f<sub>MW</sub> に対する反射RF電力をスペクトラムアナライザーで測定した結果。周波数変調（FM）のパラメータは f<sub>mf</sub> = 1 kHz、f<sub>ma</sub> = 768 MHz である。リュードベリ遷移に対応する信号として、f<sub>MW</sub> = 165 GHz 付近で f = f<sub>RF</sub> ± f<sub>mf</sub> にサイドバンド信号が現れる。</p>

<div style="margin-top:2rem;"></div>

<div class="publications">
<style>div.publications h2 { display: none; }</style>
{% bibliography --query @*[key=jennings2025rydberg] %}
</div>
