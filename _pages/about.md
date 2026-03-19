---
layout: about
title: NativQA
permalink: /
subtitle: "Framework and benchmark for culturally aligned multilingual natural question answering"
description: "NativQA is a scalable framework and benchmark for building culturally aligned multilingual natural question answering datasets in native languages for LLM evaluation and fine-tuning."
keywords: NativQA, multilingual natural question answering, culturally aligned QA, LLM benchmarking, LLM evaluation, low-resource languages, native speaker queries, nativqa-framework

#profile:
#  align: center
#  image: language_donut_chart.png
#  image_circular: false
  # crops the image to make it circular
news: true # includes a list of news items
selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page
---

<div class="landing-hero">
  <div class="landing-hero__copy">
    <p class="landing-eyebrow">Framework + benchmark for multilingual LLM evaluation</p>
    <h2>Build culturally aligned natural QA datasets grounded in native speakers and local context.</h2>
    <p class="landing-lead">
      NativQA is a scalable, language-independent framework for constructing question answering datasets in native languages. It supports both evaluation and fine-tuning of large language models, with MultiNativQA as a public benchmark built from regionally grounded, native-speaker queries.
    </p>
    <div class="landing-actions">
      <a class="btn btn-sm z-depth-0 landing-btn landing-btn--primary" href="https://gitlab.com/nativqa/nativqa-framework" target="_blank" rel="noopener noreferrer">View framework on GitLab</a>
      <a class="btn btn-sm z-depth-0 landing-btn landing-btn--secondary" href="https://pypi.org/project/nativqa-framework/" target="_blank" rel="noopener noreferrer">Install from PyPI</a>
      <a class="btn btn-sm z-depth-0 landing-btn" href="{{ '/resources/' | relative_url }}">Explore resources</a>
    </div>
    <p class="landing-install"><span>Quick install</span> <code>pip install nativqa-framework</code></p>
  </div>
  <div class="landing-hero__media">
    {% include figure.liquid loading="eager" path="assets/img/data_collection_pipeline_nativqa.png" title="NativQA data pipeline" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

### Explore resources

<div class="row">
  <div class="col-lg-6 mb-4">
    <div class="card h-100 landing-card">
      <div class="card-body">
        <p class="landing-card__kicker">Framework</p>
        <h3 class="card-title">NativQA Framework</h3>
        <p class="card-text">
          Use the framework to create culturally and regionally aligned QA datasets for multilingual LLM evaluation and tuning.
        </p>
        <div class="landing-actions">
          <a class="btn btn-sm z-depth-0 landing-btn landing-btn--primary" href="{{ '/resources/#framework' | relative_url }}">Framework resources</a>
        </div>
      </div>
    </div>
  </div>
  <div class="col-lg-6 mb-4">
    <div class="card h-100 landing-card">
      <div class="card-body">
        <p class="landing-card__kicker">Dataset</p>
        <h3 class="card-title">MultiNativQA Dataset</h3>
        <p class="card-text">
          See dataset links, download metrics, language coverage, and topic distribution in a dedicated resources page.
        </p>
        <div class="landing-actions">
          <a class="btn btn-sm z-depth-0 landing-btn landing-btn--secondary" href="{{ '/resources/#dataset' | relative_url }}">Dataset resources</a>
        </div>
      </div>
    </div>
  </div>
</div>

### Why NativQA

<div class="row">
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Native-speaker grounded</h3>
        <p class="card-text">Queries are sourced from native speakers, making evaluation data closer to real local information needs.</p>
      </div>
    </div>
  </div>
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Culturally aligned</h3>
        <p class="card-text">The benchmark emphasizes region-specific and culturally situated questions that generic QA sets often miss.</p>
      </div>
    </div>
  </div>
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Evaluation + tuning ready</h3>
        <p class="card-text">The same framework supports both benchmarking open- and closed-source LLMs and creating fine-tuning data.</p>
      </div>
    </div>
  </div>
</div>
