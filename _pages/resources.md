---
layout: page
title: resources
permalink: /resources/
description: Framework links, dataset links, and usage metrics for NativQA and MultiNativQA.
nav: true
nav_order: 1
---

The resources below collect the official links, usage indicators, and coverage details for both the framework and dataset.

## NativQA Framework {#framework}

<div class="landing-actions">
  <a class="btn btn-sm z-depth-0 landing-btn landing-btn--primary" href="https://gitlab.com/nativqa/nativqa-framework" target="_blank" rel="noopener noreferrer">GitLab repository</a>
  <a class="btn btn-sm z-depth-0 landing-btn landing-btn--secondary" href="https://pypi.org/project/nativqa-framework/" target="_blank" rel="noopener noreferrer">PyPI package</a>
</div>

<p class="landing-install"><span>Quick install</span> <code>pip install nativqa-framework</code></p>

<div class="landing-stats landing-stats--resource">
  <div class="landing-stat card">
    <div class="landing-stat__value landing-stat__value--small" id="framework-pypi-downloads">Unavailable</div>
    <p class="landing-stat__label">PyPI install downloads (public API)</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value landing-stat__value--small" id="framework-git-clones">Not public</div>
    <p class="landing-stat__label" id="framework-git-clones-label">Git clone downloads (public API)</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value" id="framework-stars">1</div>
    <p class="landing-stat__label">GitLab stars</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value" id="framework-forks">0</div>
    <p class="landing-stat__label">GitLab forks</p>
  </div>
</div>
---
## Dataset {#dataset}

### MultiNativQA Dataset {#multinativqadataset}

<div class="landing-actions">
  <a class="btn btn-sm z-depth-0 landing-btn landing-btn--primary" href="https://huggingface.co/datasets/QCRI/MultiNativQA" target="_blank" rel="noopener noreferrer">Hugging Face dataset</a>
  <a class="btn btn-sm z-depth-0 landing-btn" href="{{ '/publications/' | relative_url }}">Related publications</a>
</div>

<div class="landing-stats landing-stats--resource">
  <div class="landing-stat card">
    <div class="landing-stat__value" id="dataset-hf-downloads">3,797</div>
    <p class="landing-stat__label">Hugging Face downloads (all-time)</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value" id="dataset-hf-likes">1</div>
    <p class="landing-stat__label">Hugging Face likes</p>
  </div>
  <div class="landing-stat card">
    <div class="landing-stat__value" id="dataset-config-count">9</div>
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

#### Coverage at a glance

<div class="landing-coverage">
  <div class="landing-coverage__chart">
    {% include figure.liquid loading="eager" path="assets/img/language_donut_chart.png" title="Language distribution in MultiNativQA" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="landing-coverage__content">
    <p>
      MultiNativQA spans queries collected from native speakers across nine regions and covers everyday as well as specialized topics for more realistic multilingual evaluation.
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

<p class="resource-meta-note">Metrics are fetched from public APIs when available. Last checked: <span id="metrics-last-updated">runtime</span>.</p>

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

    setText("metrics-last-updated", new Date().toISOString().slice(0, 10));

    fetch("https://gitlab.com/api/v4/projects/nativqa%2Fnativqa-framework")
      .then(function (response) {
        if (!response.ok) {
          throw new Error("GitLab project API unavailable");
        }
        return response.json();
      })
      .then(function (data) {
        if (typeof data.star_count === "number") {
          setText("framework-stars", formatNumber(data.star_count));
        }
        if (typeof data.forks_count === "number") {
          setText("framework-forks", formatNumber(data.forks_count));
        }
      })
      .catch(function () {
        setText("framework-stars", "Unavailable");
        setText("framework-forks", "Unavailable");
      });

    fetch("https://gitlab.com/api/v4/projects/nativqa%2Fnativqa-framework/traffic/clones")
      .then(function (response) {
        if (!response.ok) {
          throw new Error("GitLab clone API unavailable");
        }
        return response.json();
      })
      .then(function (data) {
        var cloneTotal = null;
        if (typeof data.count === "number") {
          cloneTotal = data.count;
        }
        if (typeof data.total === "number") {
          cloneTotal = data.total;
        }
        if (cloneTotal === null) {
          throw new Error("Clone total not found");
        }
        setText("framework-git-clones", formatNumber(cloneTotal));
        setText("framework-git-clones-label", "Git clone downloads");
      })
      .catch(function () {
        setText("framework-git-clones", "Not public");
      });

    fetch("https://pypistats.org/api/packages/nativqa-framework/overall?mirrors=false")
      .then(function (response) {
        if (!response.ok) {
          throw new Error("PyPI stats API unavailable");
        }
        return response.json();
      })
      .then(function (data) {
        if (!data || !Array.isArray(data.data)) {
          throw new Error("PyPI stats data missing");
        }
        var total = data.data.reduce(function (sum, day) {
          if (typeof day.downloads === "number") {
            return sum + day.downloads;
          }
          return sum;
        }, 0);
        if (!total) {
          throw new Error("PyPI stats total unavailable");
        }
        setText("framework-pypi-downloads", formatNumber(total));
      })
      .catch(function () {
        setText("framework-pypi-downloads", "Unavailable");
      });

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
        if (data.cardData && Array.isArray(data.cardData.dataset_info)) {
          setText("dataset-config-count", formatNumber(data.cardData.dataset_info.length));
        }
      })
      .catch(function () {
        setText("dataset-hf-downloads", "Unavailable");
        setText("dataset-hf-likes", "Unavailable");
      });
  })();
</script>
