---
page_id: project_3
layout: page
title: Cryogenic Electronics
description: Development of cryogenic microwave sources for scalable quantum computing
img: assets/img/project3_tdo.png
importance: 3
category: research
---

To realize a large-scale quantum computer, it is necessary to connect qubits operating at cryogenic temperatures with room-temperature instruments via coaxial cables. However, the number of such cables is physically constrained, making it essential to develop measurement devices that function at low temperatures. Since qubits are controlled by microwaves, we developed a compact microwave oscillator based on a tunnel diode that operates reliably under cryogenic conditions. By connecting a tunnel diode, which exhibits negative resistance, to an LC resonator and applying a DC voltage, microwave signals are generated. The oscillator is compact (2×2 cm), operates stably at low temperatures, and exhibits smaller amplitude fluctuations than commercial microwave sources. Because amplitude stability directly impacts qubit readout fidelity, this oscillator enables more precise quantum state measurements.

<img src="{{ '/assets/img/tdo_sample_en.png' | relative_url }}" class="img-fluid rounded z-depth-1" style="width:50%; display:block; margin:0 auto;">
<p style="font-size:0.85em; color:#888; text-align:center; margin-top:0.5rem; margin-bottom:2rem;">The developed microwave oscillator successfully operates at cryogenic temperatures (10 mK). In the circuit diagram, –R represents the tunnel diode. The capacitor (C) is a varactor diode used to tune the frequency in the range of 10 MHz, and the inductor (L) is a microfabricated superconducting inductor to minimize resistive losses.</p>

<img src="{{ '/assets/img/tdo_fig2_en.png' | relative_url }}" class="img-fluid rounded z-depth-1" style="width:50%; display:block; margin:0 auto;">
<p style="font-size:0.85em; color:#888; text-align:center; margin-top:0.5rem;">Comparison of amplitude stability between a commercial microwave oscillator and the cryogenic microwave oscillator developed in this work.</p>

<div style="margin-top:2rem;"></div>

<div class="publications">
<style>div.publications h2 { display: none; }</style>
{% bibliography --query @*[key=grytsenko2024tdo] %}
</div>
