---
layout: page
title: EverydayMMQA
permalink: /resources/everydaymmqa/
description: EverydayMMQA and OASIS resource page for culturally grounded spoken visual QA.
---

<div class="landing-hero">
  <div class="landing-hero__copy">
    <p class="landing-eyebrow">Spoken visual QA</p>
    <h2>EVERYDAYMMQA: A Multilingual and Multimodal Framework for Culturally Grounded Spoken Visual QA</h2>
    <p class="landing-lead">
      EverydayMMQA is a framework for building culturally grounded spoken visual QA resources. The paper introduces OASIS, a large-scale multimodal benchmark and training resource spanning English and Arabic varieties across 18 Arab countries.
    </p>
    <div class="landing-actions">
      <a class="btn btn-sm z-depth-0 landing-btn landing-btn--primary" href="https://arxiv.org/abs/2510.06371" target="_blank" rel="noopener noreferrer">arXiv abstract</a>
      <a class="btn btn-sm z-depth-0 landing-btn landing-btn--secondary" href="https://arxiv.org/pdf/2510.06371" target="_blank" rel="noopener noreferrer">Paper PDF</a>
      <a class="btn btn-sm z-depth-0 landing-btn" href="{{ '/resources/' | relative_url }}">Back to resources</a>
    </div>
    <p class="landing-install"><span>Availability</span> Public framework and dataset links will be added here once the release is public.</p>
  </div>
  <div class="landing-hero__media">
    {% include figure.liquid loading="eager" path="assets/img/oasis_sample.png" title="OASIS sample for culturally grounded spoken visual QA" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

## Background

EverydayMMQA targets a gap in multimodal evaluation: many current models perform well on standard visual question answering but still miss culturally grounded, everyday knowledge, especially in underrepresented languages. The framework organizes the full data creation pipeline, from culturally grounded topic and query generation through country-localized image retrieval, filtering, QA generation, speech generation, translation, and quality checking. Using this pipeline, the paper develops OASIS as a benchmark and training resource for spoken visual QA.

## OASIS at a glance

<div class="landing-stats">
  <div class="landing-stat card">
    <div class="landing-stat__value">0.92M</div>
    <p class="landing-stat__label">images in the final resource</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">14.8M</div>
    <p class="landing-stat__label">QA pairs across language varieties</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">3.7M</div>
    <p class="landing-stat__label">spoken questions</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">18</div>
    <p class="landing-stat__label">Arab countries covered</p>
  </div>
</div>

<div class="landing-stats">
  <div class="landing-stat card">
    <div class="landing-stat__value">4</div>
    <p class="landing-stat__label">language varieties</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">4</div>
    <p class="landing-stat__label">input settings</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">9</div>
    <p class="landing-stat__label">top-level categories</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">31</div>
    <p class="landing-stat__label">subcategories</p>
  </div>
</div>

The paper also reports roughly 20K hours of generated speech for full coverage and 141 hours of human recordings for benchmark subsets.

## Framework pipeline

<div class="landing-coverage">
  <div class="landing-coverage__chart">
    {% include figure.liquid loading="eager" path="assets/img/everydaymmqa_framework.png" title="EverydayMMQA pipeline" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="landing-coverage__content">
    <p>
      The framework is designed as an end-to-end pipeline for culturally grounded spoken visual QA. It combines query generation, locale-aware image retrieval, filtering, multilingual QA generation, speech generation and recording, translation, and quality control into one reusable process.
    </p>
    <ul class="landing-list">
      <li>Culturally grounded topic and query generation with model-assisted filtering.</li>
      <li>Country-localized image retrieval using locale settings and license constraints.</li>
      <li>Image deduplication, filtering, categorization, and metadata generation.</li>
      <li>Open-ended, multiple-choice, and true-false QA generation per image.</li>
      <li>Speech generation, human recording, translation, and final quality checks.</li>
    </ul>
  </div>
</div>

## Dataset analysis

<div class="landing-coverage">
  <div class="landing-coverage__chart">
    {% include figure.liquid loading="eager" path="assets/img/oasis_dataset_overview.png" title="OASIS dataset overview" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="landing-coverage__content">
    <p>
      OASIS integrates speech, images, and text to support culturally grounded evaluation beyond simple object recognition. The resource spans English, Modern Standard Arabic, Egyptian Arabic, and Levantine Arabic across a balanced set of country-specific contexts.
    </p>
    <p>
      Each image is paired with four QA instances: one open-ended question, one multiple-choice question, and two true-false questions. The benchmark supports four main input settings for evaluation.
    </p>
    <div class="landing-chip-row">
      <span>Text</span>
      <span>Speech</span>
      <span>Text + Image</span>
      <span>Speech + Image</span>
    </div>
    <div class="landing-chip-row">
      <span>Open-ended</span>
      <span>Multiple-choice</span>
      <span>True / False</span>
      <span>Culturally grounded</span>
    </div>
  </div>
</div>

## Benchmarking

The paper evaluates a mix of closed and open multimodal models, including GPT-4.1, GPT-4o-audio, GPT-5, Gemini 2.5 Pro, Qwen2.5 Omni variants, Phi-4, and a fine-tuned Qwen2.5-3B-Omni model. The reported findings are consistent: visual grounding matters most, and smaller models improve substantially when the training signal aligns speech, text, and images.

<div class="row">
  <div class="col-md-6 col-xl-3 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Images shift the bottleneck</h3>
        <p class="card-text">Adding the image produces large gains across models and moves the remaining challenge from recognition toward faithful answer generation.</p>
      </div>
    </div>
  </div>
  <div class="col-md-6 col-xl-3 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Grounding narrows gaps</h3>
        <p class="card-text">Visual grounding reduces cross-lingual and dialect gaps, especially for Arabic varieties that are harder in text-only settings.</p>
      </div>
    </div>
  </div>
  <div class="col-md-6 col-xl-3 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Speech benefits most</h3>
        <p class="card-text">Images act as a modality equalizer by recovering much of the performance lost to speech and transcript noise.</p>
      </div>
    </div>
  </div>
  <div class="col-md-6 col-xl-3 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Fine-tuning helps compact models</h3>
        <p class="card-text">Light multimodal fine-tuning makes smaller systems materially more stable and competitive, particularly on audio-linked inputs.</p>
      </div>
    </div>
  </div>
</div>

## Citation

```bibtex
@article{alam2025everydaymmqa,
  title={OASIS: A Multilingual and Multimodal Framework for Culturally Grounded Spoken Visual QA},
  author={Alam, Firoj and Shahroor, Ali Ezzat and Hasan, Md. Arid and Ali, Zien Sheikh and Bhatti, Hunzalah Hassan and Kmainasi, Mohamed Bayan and Chowdhury, Shammur Absar and Mousi, Basel and Dalvi, Fahim and Durrani, Nadir and Milic-Frayling, Natasa},
  journal={arXiv preprint arXiv:2510.06371},
  year={2025}
}
```

<p class="resource-meta-note">Copyright &copy; Qatar Computing Research Institute.</p>
