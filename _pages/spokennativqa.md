---
layout: page
title: SpokenNativQA
permalink: /resources/spokennativqa/
description: SpokenNativQA resource page for multilingual everyday spoken queries for LLM evaluation.
---

<div class="landing-hero">
  <div class="landing-hero__copy">
    <p class="landing-eyebrow">Spoken QA dataset</p>
    <h2>SpokenNativQA: Multilingual Everyday Spoken Queries for LLMs</h2>
    <p class="landing-lead">
      SpokenNativQA is a multilingual and culturally aligned spoken question-answering dataset for evaluating LLMs in real-world conversational settings, where speech variability, accents, ASR errors, and local information needs all affect model behavior.
    </p>
    <div class="landing-actions">
      <a class="btn btn-sm z-depth-0 landing-btn landing-btn--primary" href="https://huggingface.co/datasets/QCRI/SpokenNativQA" target="_blank" rel="noopener noreferrer">Hugging Face dataset</a>
      <a class="btn btn-sm z-depth-0 landing-btn" href="https://www.isca-archive.org/interspeech_2025/alam25_interspeech.pdf" target="_blank" rel="noopener noreferrer">Paper PDF</a>
      <a class="btn btn-sm z-depth-0 landing-btn" href="{{ '/resources/' | relative_url }}">Back to resources</a>
    </div>
    <p class="landing-install"><span>Scope</span> Everyday spoken QA with ASR transcriptions, answers, and culturally grounded queries.</p>
  </div>
  <div class="landing-hero__media">
    {% include figure.liquid loading="eager" path="assets/img/publication_preview/spokennativqa.png" title="SpokenNativQA preview" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

## Overview

SpokenNativQA extends culturally grounded question answering into spoken interaction. The resource is designed for speech-centric evaluation rather than text-only QA, so it captures how ASR systems and LLMs behave when everyday questions are asked naturally and then evaluated with the corresponding answers.

The Interspeech 2025 paper describes the dataset as the first multilingual and culturally aligned spoken QA resource for LLM evaluation in real-world conversational settings, with approximately 33,000 naturally spoken questions and answers. The public Hugging Face dataset currently exposes Arabic and English resources with multiple ASR transcription variants.

## Dataset at a glance

<div class="landing-stats landing-stats--resource">
  <div class="landing-stat card">
    <div class="landing-stat__value" id="spokennativqa-hf-downloads">150</div>
    <p class="landing-stat__label">Hugging Face downloads</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value" id="spokennativqa-hf-likes">3</div>
    <p class="landing-stat__label">Hugging Face likes</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">33k</div>
    <p class="landing-stat__label">spoken questions and answers reported in the paper</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">8</div>
    <p class="landing-stat__label">public ASR dataset subsets</p>
  </div>
</div>

<div class="landing-stats">
  <div class="landing-stat card">
    <div class="landing-stat__value">2</div>
    <p class="landing-stat__label">languages tagged on Hugging Face</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">4</div>
    <p class="landing-stat__label">ASR systems represented</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value landing-stat__value--small">Audio + text</div>
    <p class="landing-stat__label">modalities</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value landing-stat__value--small">CC BY-NC-SA 4.0</div>
    <p class="landing-stat__label">license</p>
  </div>
</div>

## What the resource includes

<div class="row">
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Natural spoken questions</h3>
        <p class="card-text">The dataset focuses on everyday spoken queries, preserving speech variation and local context that are often missing from text-only QA benchmarks.</p>
      </div>
    </div>
  </div>
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">ASR transcription variants</h3>
        <p class="card-text">The public configs include Arabic and English subsets for Azure, Fanar Aura, Google, and Whisper ASR outputs, enabling direct study of recognition noise.</p>
      </div>
    </div>
  </div>
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Answer-grounded evaluation</h3>
        <p class="card-text">Rows include language, audio file metadata, question text, answer text, location, and ASR transcription fields for evaluating speech-to-answer pipelines.</p>
      </div>
    </div>
  </div>
</div>

## Dataset fields

The Hugging Face viewer shows fields for language, dataset id, audio file name and path, the original question, answer, location, and question ASR transcription. This makes the resource useful for benchmarking both ASR systems and downstream LLM answer quality.

<div class="landing-chip-row">
  <span>Question answering</span>
  <span>Audio</span>
  <span>Text</span>
  <span>Arabic</span>
  <span>English</span>
  <span>ASR robustness</span>
  <span>Cultural alignment</span>
</div>

## Citation

{% raw %}
<pre><code class="language-bibtex">@inproceedings{alam25_interspeech,
  title     = {{SpokenNativQA: Multilingual Everyday Spoken Queries for LLMs}},
  author    = {Firoj Alam and Md Arid Hasan and Shammur Absar Chowdhury},
  year      = {2025},
  booktitle = {{Interspeech 2025}},
  pages     = {2685--2689},
  doi       = {10.21437/Interspeech.2025-2011},
  issn      = {2958-1796},
}</code></pre>
{% endraw %}

<p class="resource-meta-note">Metrics are fetched from public APIs when available. Last checked: <span id="spokennativqa-metrics-last-updated">runtime</span>.</p>

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

    setText("spokennativqa-metrics-last-updated", new Date().toISOString().slice(0, 10));

    fetch("https://huggingface.co/api/datasets/QCRI/SpokenNativQA?expand[]=downloadsAllTime&expand[]=likes")
      .then(function (response) {
        if (!response.ok) {
          throw new Error("Hugging Face API unavailable");
        }
        return response.json();
      })
      .then(function (data) {
        if (typeof data.downloadsAllTime === "number") {
          setText("spokennativqa-hf-downloads", formatNumber(data.downloadsAllTime));
        } else if (typeof data.downloads === "number") {
          setText("spokennativqa-hf-downloads", formatNumber(data.downloads));
        }
        if (typeof data.likes === "number") {
          setText("spokennativqa-hf-likes", formatNumber(data.likes));
        }
      })
      .catch(function () {
        setText("spokennativqa-hf-downloads", "Unavailable");
        setText("spokennativqa-hf-likes", "Unavailable");
      });
  })();
</script>
