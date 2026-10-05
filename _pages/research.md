---
layout: page
title: Research
permalink: /research/
nav: true
nav_order: 6
---

<style>
.research-intro {
  max-width: 48rem;
  line-height: 1.7;
  margin-bottom: 0.8rem;
}

.research-questions {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 0.75rem;
  margin-bottom: 2rem;
}

.research-question {
  background: var(--research-topic-bg);
  border-left: 4px solid var(--research-topic-accent);
  border-radius: 0.3rem;
  min-height: 7rem;
  padding: 0.85rem 1rem;
}

.research-question-label {
  color: var(--research-topic-accent);
  display: block;
  font-size: 0.74rem;
  font-weight: 700;
  letter-spacing: 0.04em;
  margin-bottom: 0.45rem;
  text-transform: uppercase;
}

.research-question-text {
  color: var(--global-text-color);
  display: block;
  font-size: 0.96rem;
  line-height: 1.5;
}

.research-topic--alignment {
  --research-topic-bg: #eef0ff;
  --research-topic-accent: #6256a8;
}

.research-topic--reliability {
  --research-topic-bg: #e7f4ef;
  --research-topic-accent: #276f59;
}

.research-topic--foundations {
  --research-topic-bg: #fff2e2;
  --research-topic-accent: #945b1a;
}

html[data-theme="dark"] .research-topic--alignment {
  --research-topic-bg: #29283c;
  --research-topic-accent: #bdb4fa;
}

html[data-theme="dark"] .research-topic--reliability {
  --research-topic-bg: #20342e;
  --research-topic-accent: #8bd2b5;
}

html[data-theme="dark"] .research-topic--foundations {
  --research-topic-bg: #392d22;
  --research-topic-accent: #e8bc85;
}

.research-theme {
  border-top: 1px solid var(--global-divider-color);
  margin-top: 1.8rem;
  padding-top: 1.35rem;
}

.research-theme h2 {
  background: var(--research-topic-bg);
  border-left: 4px solid var(--research-topic-accent);
  border-radius: 0.3rem;
  font-size: 1.45rem;
  margin-bottom: 0.8rem;
  padding: 0.45rem 0.85rem;
}

.research-theme > p {
  max-width: 48rem;
  margin-bottom: 0.85rem;
}

.research-papers {
  font-size: 0.94rem;
  line-height: 1.55;
  margin: 0.65rem 0 0;
  padding-left: 1.3rem;
}

.research-papers li {
  margin-bottom: 0.4rem;
}

.research-paper-note {
  color: var(--global-text-color-light);
}

.research-footer {
  border-top: 1px solid var(--global-divider-color);
  margin-top: 1.8rem;
  padding-top: 1rem;
}

@media (max-width: 700px) {
  .research-questions {
    grid-template-columns: 1fr;
    gap: 0.55rem;
  }

  .research-question {
    min-height: 0;
  }
}
</style>

<p class="research-intro">My research focuses on three questions:</p>

<div class="research-questions">
  <div class="research-question research-topic--alignment">
    <span class="research-question-label">AI Alignment</span>
    <span class="research-question-text">How do AI systems learn to generalise?</span>
  </div>
  <div class="research-question research-topic--reliability">
    <span class="research-question-label">Reliable AI &amp; Safety</span>
    <span class="research-question-text">How can capable systems be made reliable and safe?</span>
  </div>
  <div class="research-question research-topic--foundations">
    <span class="research-question-label">Statistical Foundations for AI</span>
    <span class="research-question-text">What statistical principles explain and improve their behaviour?</span>
  </div>
</div>

<section class="research-theme research-topic--alignment" aria-labelledby="research-alignment">
  <h2 id="research-alignment">AI Alignment</h2>
  <p>I use alignment in a broad sense: how can we develop models and agents that gain useful capabilities and generalise beyond familiar tasks and environments? My work here spans model adaptation, reasoning, embodied action, and agents that combine evidence and tools to solve complex tasks. Safety can also be part of what a system learns, rather than only an external safeguard.</p>
  <ul class="research-papers">
    <li><a href="https://arxiv.org/abs/2605.30484">ELAN4D</a> <span class="research-paper-note">— generalisation in vision-language-action models; CoRL 2026.</span></li>
    <li><a href="https://arxiv.org/abs/2605.24697">The Path Matters</a> <span class="research-paper-note">— a token-commitment policy learned from agreement with final decoded tokens, improving the speed–quality trade-off in diffusion language models; preprint, 2026.</span></li>
    <li><a href="https://arxiv.org/abs/2606.02747">Plan2Map</a> <span class="research-paper-note">— a document-grounded geospatial agent for planning records; preprint, 2026.</span></li>
  </ul>
</section>

<section class="research-theme research-topic--reliability" aria-labelledby="research-reliability">
  <h2 id="research-reliability">Reliable AI &amp; Safety</h2>
  <p>Capability alone does not make an AI system trustworthy. I study how to measure uncertainty, detect failures, evaluate systems when human verification is difficult, and make model and agent behaviour more stable and controllable. Much of this work starts with an existing system and adds calibration, monitoring, or practical safeguards.</p>
  <ul class="research-papers">
    <li><a href="https://proceedings.mlr.press/v306/marro26a.html">Benchmarking at the Edge of Comprehension</a> <span class="research-paper-note">— evaluation with humans as bounded verifiers; ICML 2026.</span></li>
    <li><a href="https://arxiv.org/abs/2608.01460">Conformalized Large Language Models under Configuration Shift</a> <span class="research-paper-note">— calibration under changing inference settings; EMNLP 2026.</span></li>
    <li><a href="https://proceedings.iclr.cc/paper_files/paper/2026/hash/10272bfd0371ef960ec557ed6c866058-Abstract-Conference.html">TraceDet</a> <span class="research-paper-note">— hallucination detection in diffusion language models; ICLR 2026.</span></li>
    <li><a href="https://proceedings.iclr.cc/paper_files/paper/2026/hash/a79875cc0d046ce7ce65f03f3affaa9e-Abstract-Conference.html">BiasBusters</a> <span class="research-paper-note">— tool-selection bias in agents; ICLR 2026.</span></li>
    <li><a href="https://arxiv.org/abs/2602.00388">Safer by Diffusion, Broken by Context</a> <span class="research-paper-note">— safety failure modes in diffusion language models; ICML 2026 workshop.</span></li>
  </ul>
</section>

<section class="research-theme research-topic--foundations" aria-labelledby="research-foundations">
  <h2 id="research-foundations">Statistical Foundations for AI</h2>
  <p>I develop causal and statistical approaches to understand and improve learning under shifts, interventions, and uncertainty. This includes identifying when generalisation is possible and translating structural assumptions into better learning methods.</p>
  <ul class="research-papers">
    <li><a href="https://proceedings.mlr.press/v306/yu26bx.html">Causal Fine-Tuning under Latent Confounded Shift</a> <span class="research-paper-note">— causal identification and robust adaptation; ICML 2026.</span></li>
    <li><a href="https://proceedings.neurips.cc/paper_files/paper/2024/hash/d10c7e24c96db4b222688efd11b02940-Abstract-Conference.html">Structured Learning of Compositional Sequential Interventions</a> <span class="research-paper-note">— compositional intervention learning; NeurIPS 2024.</span></li>
    <li><a href="https://proceedings.neurips.cc/paper_files/paper/2023/hash/88139fdcc82fc597090620d77b023282-Abstract-Conference.html">Intervention Generalization: A View from Factor Graph Models</a> <span class="research-paper-note">— identifying outcomes under new interventions; NeurIPS 2023.</span></li>
  </ul>
</section>

<p class="research-footer">This page highlights work connected to my current research themes; for a full and continually updated publication list, please visit my <a href="https://scholar.google.com/citations?user=L8tFzjgAAAAJ&amp;hl=en">Google Scholar</a> profile.</p>
