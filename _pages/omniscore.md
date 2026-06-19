---
layout: page
title: OmniScore
permalink: /resources/omniscore/
description: OmniScore resource page for deterministic multilingual generative text evaluation metrics.
---

<div class="landing-hero landing-hero--single">
  <div class="landing-hero__copy">
    <p class="landing-eyebrow">Evaluation toolkit</p>
    <h2>OmniScore: Deterministic Metrics for Multilingual Generative Text Evaluation</h2>
    <p class="landing-lead">
      OmniScore is a family of deterministic learned metrics for multilingual generated-text evaluation. It is designed as a practical alternative to costly and prompt-sensitive LLM-as-a-judge workflows, while keeping the speed and consistency of model-based scoring.
    </p>
    <div class="landing-actions">
      <a class="btn btn-sm z-depth-0 landing-btn landing-btn--primary" href="https://pypi.org/project/omniscore/" target="_blank" rel="noopener noreferrer">PyPI package</a>
      <a class="btn btn-sm z-depth-0 landing-btn landing-btn--secondary" href="https://huggingface.co/datasets/QCRI/OmniScore-Data" target="_blank" rel="noopener noreferrer">Hugging Face data</a>
      <a class="btn btn-sm z-depth-0 landing-btn" href="https://huggingface.co/collections/QCRI/omniscore" target="_blank" rel="noopener noreferrer">Hugging Face collection</a>
      <a class="btn btn-sm z-depth-0 landing-btn" href="https://arxiv.org/abs/2604.05083" target="_blank" rel="noopener noreferrer">arXiv</a>
      <a class="btn btn-sm z-depth-0 landing-btn" href="{{ '/resources/' | relative_url }}">Back to resources</a>
    </div>
    <p class="landing-install"><span>Quick install</span> <code>pip install omniscore</code></p>
  </div>
</div>

## Overview

LLM-as-a-judge evaluation can be expensive, slow, and sensitive to prompt design, language, and aggregation choices. OmniScore addresses this with small deterministic learned metrics that approximate LLM-judge behavior while providing reproducible, low-latency scores for generated text.

The paper reports large-scale synthetic supervision across 107 languages and evaluates the approach on manually annotated examples. The released resources include a Python package, model checkpoints, and the OmniScore-Data dataset for training and evaluation workflows.

## Resource at a glance

<div class="landing-stats landing-stats--resource">
  <div class="landing-stat card">
    <div class="landing-stat__value" id="omniscore-hf-downloads">247</div>
    <p class="landing-stat__label">Hugging Face dataset downloads</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value" id="omniscore-hf-likes">1</div>
    <p class="landing-stat__label">Hugging Face dataset likes</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">581k</div>
    <p class="landing-stat__label">rows in OmniScore-Data</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">99</div>
    <p class="landing-stat__label">language values in the data viewer</p>
  </div>
</div>

<div class="landing-stats">
  <div class="landing-stat card">
    <div class="landing-stat__value">6</div>
    <p class="landing-stat__label">task values in OmniScore-Data</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">107</div>
    <p class="landing-stat__label">languages reported for training supervision</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value">8,617</div>
    <p class="landing-stat__label">manual annotations reported in the paper</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value landing-stat__value--small">MIT</div>
    <p class="landing-stat__label">package license</p>
  </div>
</div>

## What the resource includes

<div class="row">
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Python and CLI scoring</h3>
        <p class="card-text">The PyPI package supports both Python APIs and a command line interface for scoring generated text with hosted OmniScore checkpoints.</p>
      </div>
    </div>
  </div>
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Released data</h3>
        <p class="card-text">OmniScore-Data contains train, validation, and test splits with input, output, task, language, and multi-dimensional label fields.</p>
      </div>
    </div>
  </div>
  <div class="col-md-4 mb-4">
    <div class="card h-100 landing-mini-card">
      <div class="card-body">
        <h3 class="card-title">Model collection</h3>
        <p class="card-text">The Hugging Face collection links the paper, released data, and checkpoints such as QCRI/OmniScore-mxbai and QCRI/OmniScore-deberta-v3.</p>
      </div>
    </div>
  </div>
</div>

## Dataset and scoring dimensions

The Hugging Face data viewer lists 581k rows with train, validation, and test splits. It exposes six task values and 99 language values, with labels for scoring dimensions such as clarity, faithfulness, informativeness, and plausibility.

<div class="landing-chip-row">
  <span>Question answering</span>
  <span>Translation</span>
  <span>Summarization</span>
  <span>Clarity</span>
  <span>Faithfulness</span>
  <span>Informativeness</span>
  <span>Plausibility</span>
</div>

## Quick usage

```python
from omniscore import OmniScorer, get_example

example = get_example("QCRI/OmniScore-deberta-v3")
scorer = OmniScorer("QCRI/OmniScore-deberta-v3")

result = scorer.score(
    predictions=example.prediction,
    sources=example.source,
    references=example.reference,
    tasks=example.task,
)
print(result.to_list())
```

```bash
omniscore \
  --model QCRI/OmniScore-deberta-v3 \
  --prediction "Microsoft releases detailed model documentation." \
  --source "Full article text goes here." \
  --task headline_evaluation \
  --pretty
```

## Citation

{% raw %}
<pre><code class="language-bibtex">@article{alam2026llmasajudgedeterministicmetricsmultilingual,
  title={Beyond LLM-as-a-Judge: Deterministic Metrics for Multilingual Generative Text Evaluation},
  author={Alam, Firoj and Bhatia, Gagan and Laskar, Sahinur Rahman and Chowdhury, Shammur Absar},
  journal={arXiv preprint arXiv:2604.05083},
  year={2026},
  url={https://arxiv.org/abs/2604.05083}
}</code></pre>
{% endraw %}

<p class="resource-meta-note">Metrics are fetched from public APIs when available. Last checked: <span id="omniscore-metrics-last-updated">runtime</span>.</p>

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

    setText("omniscore-metrics-last-updated", new Date().toISOString().slice(0, 10));

    fetch("https://huggingface.co/api/datasets/QCRI/OmniScore-Data?expand[]=downloadsAllTime&expand[]=likes")
      .then(function (response) {
        if (!response.ok) {
          throw new Error("Hugging Face API unavailable");
        }
        return response.json();
      })
      .then(function (data) {
        if (typeof data.downloadsAllTime === "number") {
          setText("omniscore-hf-downloads", formatNumber(data.downloadsAllTime));
        } else if (typeof data.downloads === "number") {
          setText("omniscore-hf-downloads", formatNumber(data.downloads));
        }
        if (typeof data.likes === "number") {
          setText("omniscore-hf-likes", formatNumber(data.likes));
        }
      })
      .catch(function () {
        setText("omniscore-hf-downloads", "Unavailable");
        setText("omniscore-hf-likes", "Unavailable");
      });
  })();
</script>
