---
page_id: project_1
layout: page
title: Rydberg Transitions
description: Quantum capacitance induced by Rydberg transitions
img: assets/img/rydberg_rf.png
importance: 1
category: research
---

<div class="alert alert-warning" role="alert" style="font-size:0.9em;">
  🚧 This page is under construction.
</div>

Electrons on liquid helium offer a clean platform for quantum computing, with spin states expected to have long coherence times. However, spin-state detection remains challenging. A promising approach maps the spin state onto a Rydberg state, detectable via an LC tank circuit with high sensitivity and small footprint. As a proof of concept, we detect Rydberg transitions of an electron ensemble using frequency-modulated microwaves. Adiabatic transitions induce measurable quantum capacitance. The achieved sensitivity allows resolving the Rydberg transition of a single electron, paving the way for scalable spin-state readout and helium-based quantum technologies.

<img src="{{ '/assets/img/rydberg_rf.png' | relative_url }}" class="img-fluid rounded z-depth-1" style="width:75%; display:block; margin:0 auto;">
<p style="font-size:0.85em; color:#888; text-align:center; margin-top:0.5rem;">Reflected RF power measured with a spectrum analyzer as a function of the microwave (MW) carrier frequency f<sub>MW</sub>. The frequency modulation (FM) parameters are f<sub>mf</sub> = 1 kHz and f<sub>ma</sub> = 768 MHz. Sideband signals appear at f = f<sub>RF</sub> ± f<sub>mf</sub> around f<sub>MW</sub> = 165 GHz, corresponding to the Rydberg transition.</p>

<div style="margin-top:2rem;"></div>

<div class="publications" style="--publications-heading-display: none;">
<style>div.publications h2 { display: none; }</style>
{% bibliography --query @*[key=jennings2025rydberg] %}
</div>
