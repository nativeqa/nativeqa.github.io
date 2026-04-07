---
layout: page
title: MENASpeechBank
permalink: /resources/menaspeechbank/
description: MENASpeechBank resource page for Arabic and MENA-focused AudioLLM speech resources.
---

<div class="landing-hero landing-hero--single">
  <div class="landing-hero__copy">
    <p class="landing-eyebrow">AudioLLM resource</p>
    <h2>MENASpeechBank: A Reference Voice Bank with Persona-Conditioned Multi-Turn Conversations for AudioLLMs</h2>
    <p class="landing-lead">
      Building better resources for AudioLLMs through the lens of Arabic, MENASpeechBank combines a curated voice bank and a large persona-conditioned conversation pipeline to support evaluation in culturally grounded, multi-turn speech settings.
    </p>
    <div class="landing-actions">
      <a class="btn btn-sm z-depth-0 landing-btn landing-btn--primary" href="https://huggingface.co/datasets/QCRI/MenaSpeechBank" target="_blank" rel="noopener noreferrer">Hugging Face dataset</a>
      <a class="btn btn-sm z-depth-0 landing-btn landing-btn--secondary" href="https://arxiv.org/abs/2602.07036" target="_blank" rel="noopener noreferrer">arXiv abstract</a>
      <a class="btn btn-sm z-depth-0 landing-btn" href="https://arxiv.org/pdf/2602.07036" target="_blank" rel="noopener noreferrer">Paper PDF</a>
      <a class="btn btn-sm z-depth-0 landing-btn" href="{{ '/resources/' | relative_url }}">Back to resources</a>
    </div>
    <p class="landing-install"><span>Scope</span> Arabic and MENA speech resources with an extensible framework for other languages.</p>
  </div>
</div>

## Overview

The development of AudioLLMs for low-resource languages depends not only on model capability, but also on speech resources that capture dialect diversity, speaker variation, and realistic conversational interaction. MENASpeechBank addresses this need for Arabic and the MENA region by pairing a reference voice bank with a large synthetic conversation pipeline designed for persona-grounded, multi-turn evaluation.

More broadly, MENASpeechBank is not only a resource for Arabic. The pipeline is designed to be reusable for building **similar AudioLLM resources in other languages** where real conversational speech data is scarce.

## Resource at a glance

<div class="landing-stats landing-stats--resource">
  <div class="landing-stat card">
    <div class="landing-stat__value" id="menaspeechbank-hf-downloads">3,915</div>
    <p class="landing-stat__label">Hugging Face downloads (all-time)</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">17,641</div>
    <p class="landing-stat__label">reference utterances</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">124</div>
    <p class="landing-stat__label">speakers in the voice bank</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">18</div>
    <p class="landing-stat__label">countries represented</p>
  </div>
</div>

<div class="landing-stats">
  <div class="landing-stat card">
    <div class="landing-stat__value">469</div>
    <p class="landing-stat__label">personas</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">900</div>
    <p class="landing-stat__label">topics</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">4,521</div>
    <p class="landing-stat__label">conversation scenarios</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">417k</div>
    <p class="landing-stat__label">multi-turn dialogues</p>
  </div>
</div>

## What the resource includes

<div class="row">
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Reference voice bank</h3>
        <p class="card-text">A curated speech bank with 17,641 utterances from 124 speakers across 18 MENA countries, covering English, Modern Standard Arabic, and regional Arabic varieties.</p>
      </div>
    </div>
  </div>
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Persona-conditioned conversations</h3>
        <p class="card-text">A large synthetic pipeline builds 469 personas, 900 topics, and 4,521 scenarios to generate approximately 417,000 multi-turn dialogues grounded in realistic assistant interactions.</p>
      </div>
    </div>
  </div>
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Extensible framework</h3>
        <p class="card-text">The design is not limited to Arabic. MENASpeechBank also serves as a template for building AudioLLM resources in other low-resource and dialect-rich languages.</p>
      </div>
    </div>
  </div>
</div>

## Why it matters for AudioLLMs

MENASpeechBank is designed to support the development of conversational speech datasets for AudioLLMs. It is intended to enable the development and evaluation of models that can maintain conversational context, adapt to speaker characteristics, and respond appropriately in culturally grounded interactions that reflect real language use across the MENA region.

<div class="landing-chip-row">
  <span>Arabic</span>
  <span>MENA</span>
  <span>Persona-grounded</span>
  <span>Multi-turn</span>
  <span>Dialect diversity</span>
  <span>Speaker variation</span>
  <span>AudioLLMs</span>
</div>

## Framework

The paper describes a controllable pipeline that constructs persona profiles, defines conversational scenarios, matches personas to scenarios, generates role-play conversations, and synthesizes user turns while preserving speaker identity through reference audio. This makes the resource useful not only for benchmark creation, but also for studying how model behavior changes across speakers, dialects, and interaction settings.

## Citation

```bibtex
@article{ali2026menaspeechbank,
  title={MENASpeechBank: A Reference Voice Bank with Persona-Conditioned Multi-Turn Conversations for AudioLLMs},
  author={Ali, Zien Sheikh and Bhatti, Hunzalah Hassan and Nandi, Rabindra Nath and Chowdhury, Shammur Absar and Alam, Firoj},
  journal={arXiv preprint arXiv:2602.07036},
  year={2026}
}
```

<p class="resource-meta-note">Metrics are fetched from public APIs when available. Last checked: <span id="menaspeechbank-metrics-last-updated">runtime</span>.</p>

<p class="resource-meta-note">Copyright &copy; Qatar Computing Research Institute.</p>

<script>
  (function () {
    function setText(id, value) {
      var element = document.getElementById(id);
      if (element) {
        element.textContent = value;
      }
    }

    function formatNumber(value) {
      if (typeof value !== "number" || Number.isNaN(value)) {
        return "Unavailable";
      }
      return value.toLocaleString("en-US");
    }

    setText("menaspeechbank-metrics-last-updated", new Date().toISOString().slice(0, 10));

    fetch("https://huggingface.co/api/datasets/QCRI/MenaSpeechBank?expand[]=downloadsAllTime")
      .then(function (response) {
        if (!response.ok) {
          throw new Error("Hugging Face API unavailable");
        }
        return response.json();
      })
      .then(function (data) {
        if (typeof data.downloadsAllTime === "number") {
          setText("menaspeechbank-hf-downloads", formatNumber(data.downloadsAllTime));
        } else if (typeof data.downloads === "number") {
          setText("menaspeechbank-hf-downloads", formatNumber(data.downloads));
        }
      })
      .catch(function () {
        setText("menaspeechbank-hf-downloads", "Unavailable");
      });
  })();
</script>
