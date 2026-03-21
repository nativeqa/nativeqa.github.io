---
layout: about
title: about
permalink: /
subtitle: "Framework, datasets, and benchmarks for culturally aligned multilingual and multimodal QA"
description: "NativMMQA brings together a framework and public benchmark resources for culturally aligned multilingual and multimodal question answering, supporting LLM evaluation and fine-tuning."
keywords: NativMMQA, NativQA, nativqa-framework, MultiNativQA, EverydayMMQA, OASIS, multilingual QA, multimodal QA, culturally aligned QA, spoken visual QA, LLM benchmarking

#profile:
#  align: center
#  image: language_donut_chart.png
#  image_circular: false
  # crops the image to make it circular
news: true # includes a list of news items
selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page
---

<div class="landing-hero landing-hero--single">
  <div class="landing-hero__copy">
    <p class="landing-eyebrow">Framework + datasets + benchmarks</p>
    <h2>Build and evaluate culturally grounded QA resources across languages and modalities.</h2>
    <p class="landing-lead">
      NativMMQA brings together the NativQA Framework and public benchmark resources for culturally aligned evaluation. Our work currently spans MultiNativQA for multilingual natural QA and EverydayMMQA/OASIS for culturally grounded spoken visual QA, giving one entry point for building, benchmarking, and extending datasets for LLM evaluation and fine-tuning.
    </p>
    <div class="landing-actions">
      <a class="btn btn-sm z-depth-0 landing-btn landing-btn--primary" href="{{ '/resources/' | relative_url }}">Explore resources</a>
      <a class="btn btn-sm z-depth-0 landing-btn landing-btn--secondary" href="https://gitlab.com/nativqa/nativqa-framework" target="_blank" rel="noopener noreferrer">View framework on GitLab</a>
      <a class="btn btn-sm z-depth-0 landing-btn" href="https://pypi.org/project/nativqa-framework/" target="_blank" rel="noopener noreferrer">Install from PyPI</a>
    </div>
  </div>
</div>

### Explore the ecosystem

<div class="row">
  <div class="col-lg-4 mb-4">
    <div class="card h-100 landing-card">
      <div class="card-body">
        <p class="landing-card__kicker">Framework</p>
        <h3 class="card-title">NativQA Framework</h3>
        <p class="card-text">
          Use the framework to create culturally and regionally aligned QA datasets for multilingual and multimodal model evaluation and tuning.
        </p>
        <div class="landing-actions">
          <a class="btn btn-sm z-depth-0 landing-btn landing-btn--primary" href="{{ '/resources/#framework' | relative_url }}">Framework resources</a>
        </div>
      </div>
    </div>
  </div>
  <div class="col-lg-4 mb-4">
    <div class="card h-100 landing-card">
      <div class="card-body">
        <p class="landing-card__kicker">Dataset</p>
        <h3 class="card-title">MultiNativQA</h3>
        <p class="card-text">
          See links, live download metrics, language coverage, regional scope, and topic distribution for the multilingual natural QA benchmark.
        </p>
        <div class="landing-actions">
          <a class="btn btn-sm z-depth-0 landing-btn landing-btn--secondary" href="{{ '/resources/multinativqa/' | relative_url }}">Dataset resources</a>
        </div>
      </div>
    </div>
  </div>
  <div class="col-lg-4 mb-4">
    <div class="card h-100 landing-card">
      <div class="card-body">
        <p class="landing-card__kicker">Spoken visual QA</p>
        <h3 class="card-title">EverydayMMQA / OASIS</h3>
        <p class="card-text">
          Explore the multilingual and multimodal framework for culturally grounded spoken visual QA, with paper context, dataset scale, and benchmark takeaways.
        </p>
        <div class="landing-actions">
          <a class="btn btn-sm z-depth-0 landing-btn" href="{{ '/resources/everydaymmqa/' | relative_url }}">Open resource page</a>
        </div>
      </div>
    </div>
  </div>
</div>

### Why this work matters

<div class="row">
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Native-speaker grounded</h3>
        <p class="card-text">Queries are sourced from native speakers and local contexts, making the data closer to real information needs than generic prompt collections.</p>
      </div>
    </div>
  </div>
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Multilingual and multimodal</h3>
        <p class="card-text">The site now covers both natural QA and spoken visual QA, making the resource collection broader than a single benchmark page.</p>
      </div>
    </div>
  </div>
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Reusable across workflows</h3>
        <p class="card-text">The same framework and resource family support benchmarking, analysis, and the creation of fine-tuning data for culturally aligned systems.</p>
      </div>
    </div>
  </div>
</div>
