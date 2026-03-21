---
layout: page
title: MultiNativQA
permalink: /resources/multinativqa/
description: MultiNativQA dataset resource page for multilingual culturally aligned natural question answering.
---

<div class="landing-hero">
  <div class="landing-hero__copy">
    <p class="landing-eyebrow">Dataset resource</p>
    <h2>MultiNativQA: multilingual culturally aligned natural QA benchmark</h2>
    <p class="landing-lead">
      MultiNativQA is a multilingual benchmark built with native-speaker queries and local context for more realistic evaluation of large language models. It supports both benchmarking and fine-tuning across languages with different resource levels.
    </p>
    <div class="landing-actions">
      <a class="btn btn-sm z-depth-0 landing-btn landing-btn--primary" href="https://huggingface.co/datasets/QCRI/MultiNativQA" target="_blank" rel="noopener noreferrer">Hugging Face dataset</a>
      <a class="btn btn-sm z-depth-0 landing-btn landing-btn--secondary" href="https://aclanthology.org/2025.findings-acl.770/" target="_blank" rel="noopener noreferrer">ACL 2025 paper</a>
      <a class="btn btn-sm z-depth-0 landing-btn" href="{{ '/resources/' | relative_url }}">Back to resources</a>
    </div>
    <p class="landing-install"><span>Built with</span> <a href="https://gitlab.com/nativqa/nativqa-framework" target="_blank" rel="noopener noreferrer">NativQA Framework</a></p>
  </div>
  <div class="landing-hero__media">
    {% include figure.liquid loading="eager" path="assets/img/data_collection_pipeline_nativqa.png" title="MultiNativQA data collection pipeline" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

## Overview

MultiNativQA is designed to evaluate large language models with queries that reflect how native speakers ask questions in their own languages and regions. Instead of relying on generic or synthetic prompts, the benchmark emphasizes cultural alignment, local knowledge, and realistic information needs across diverse linguistic settings.

## Dataset at a glance

<div class="landing-stats landing-stats--resource">
  <div class="landing-stat card">
    <div class="landing-stat__value" id="dataset-hf-downloads">3,828</div>
    <p class="landing-stat__label">Hugging Face downloads (all-time)</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value" id="dataset-hf-likes">1</div>
    <p class="landing-stat__label">Hugging Face likes</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">9</div>
    <p class="landing-stat__label">dataset configs</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value landing-stat__value--small">CC BY-NC-SA 4.0</div>
    <p class="landing-stat__label">license</p>
  </div>
</div>

<div class="landing-stats">
  <div class="landing-stat card">
    <div class="landing-stat__value">64k+</div>
    <p class="landing-stat__label">manually annotated QA pairs</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">7</div>
    <p class="landing-stat__label">languages represented</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">9</div>
    <p class="landing-stat__label">regions covered</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">18</div>
    <p class="landing-stat__label">seed topics for query collection</p>
  </div>
</div>

## Coverage at a glance

<div class="landing-coverage">
  <div class="landing-coverage__chart">
    {% include figure.liquid loading="eager" path="assets/img/language_donut_chart.png" title="Language distribution in MultiNativQA" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="landing-coverage__content">
    <p>
      MultiNativQA spans native-speaker queries collected across nine regions and covers both everyday and specialized topics to better stress-test multilingual model behavior in realistic settings.
    </p>
    <div class="landing-chip-row landing-chip-row--topics">
      <span>Animal</span>
      <span>Business</span>
      <span>Cloth</span>
      <span>Education</span>
      <span>Events</span>
      <span>Food &amp; Drinks</span>
      <span>General</span>
      <span>Geography</span>
      <span>Immigration</span>
      <span>Language</span>
      <span>Literature</span>
      <span>Names &amp; Persons</span>
      <span>Plants</span>
      <span>Religion</span>
      <span>Sports &amp; Games</span>
      <span>Tradition</span>
      <span>Travel</span>
      <span>Weather</span>
    </div>
  </div>
</div>

## Why this benchmark matters

<div class="row">
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Native-speaker grounded</h3>
        <p class="card-text">Queries come from native speakers, which makes the benchmark closer to real local information needs than template-heavy alternatives.</p>
      </div>
    </div>
  </div>
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Region-aware evaluation</h3>
        <p class="card-text">The dataset emphasizes cultural and regional variation that multilingual models often miss when evaluation sets are too generic.</p>
      </div>
    </div>
  </div>
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Evaluation and tuning ready</h3>
        <p class="card-text">The benchmark supports both model evaluation and downstream fine-tuning workflows built on culturally aligned QA data.</p>
      </div>
    </div>
  </div>
</div>

## Citation

```bibtex
@inproceedings{hasan-etal-2025-nativqa,
  title = "{NativQA:} Multilingual Culturally-Aligned Natural Query for {LLM}s",
  author = "Hasan, Md. Arid and Hasanain, Maram and Ahmad, Fatema and Laskar, Sahinur Rahman and Upadhyay, Sunaya and Sukhadia, Vrunda N and Kutlu, Mucahid and Chowdhury, Shammur Absar and Alam, Firoj",
  booktitle = "Findings of the Association for Computational Linguistics: ACL 2025",
  year = "2025",
  address = "Vienna, Austria",
  publisher = "Association for Computational Linguistics",
  url = "https://aclanthology.org/2025.findings-acl.770/",
  doi = "10.18653/v1/2025.findings-acl.770",
  pages = "14886--14909"
}
```

<p class="resource-meta-note">Metrics are fetched from public APIs when available. Last checked: <span id="dataset-metrics-last-updated">runtime</span>.</p>

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

    setText("dataset-metrics-last-updated", new Date().toISOString().slice(0, 10));

    fetch("https://huggingface.co/api/datasets/QCRI/MultiNativQA?expand[]=downloadsAllTime&expand[]=likes")
      .then(function (response) {
        if (!response.ok) {
          throw new Error("Hugging Face API unavailable");
        }
        return response.json();
      })
      .then(function (data) {
        if (typeof data.downloadsAllTime === "number") {
          setText("dataset-hf-downloads", formatNumber(data.downloadsAllTime));
        } else if (typeof data.downloads === "number") {
          setText("dataset-hf-downloads", formatNumber(data.downloads));
        }
        if (typeof data.likes === "number") {
          setText("dataset-hf-likes", formatNumber(data.likes));
        }
      })
      .catch(function () {
        setText("dataset-hf-downloads", "Unavailable");
        setText("dataset-hf-likes", "Unavailable");
      });
  })();
</script>
