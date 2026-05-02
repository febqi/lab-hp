---
page_id: project_3
layout: page
title: 極低温エレクトロニクス
description: 量子ビット数の拡張に向けた極低温マイクロ波源の開発
img: assets/img/project3_tdo.png
importance: 3
category: research
---

<div class="alert alert-warning" role="alert" style="font-size:0.9em;">
  🚧 このページは現在作成中です。
</div>

量子コンピュータを大規模化するためには、室温と極低温の間の複雑な配線を不要とする極低温動作の制御エレクトロニクスが必要です。

トンネルダイオード発振器（TDO）を用いた極低温マイクロ波源を開発しており、商用の室温源よりも優れた振幅安定性を実現しました。

<img src="{{ '/assets/img/TDO.png' | relative_url }}" class="img-fluid rounded z-depth-1" style="width:75%;">

**主な研究テーマ：**

- TDOベースの極低温マイクロ波源
- 極低温信号生成・増幅
- 量子ビット制御システムへの統合

<div style="margin-top:2rem;"></div>

<div class="publications">
{% bibliography --query @*[key=grytsenko2024tdo] %}
</div>
