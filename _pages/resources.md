---
layout: page
title: resources
permalink: /resources/
description: Framework links and dedicated resource pages for NativQA datasets and related work.
nav: true
nav_order: 1
---

The resources below collect the official framework links and dedicated pages for datasets and related work.

## Resource pages

<div class="row">
  <div class="col-lg-6 mb-4">
    <div class="card h-100 landing-card">
      <div class="card-body">
        <p class="landing-card__kicker">Dataset</p>
        <h3 class="card-title">MultiNativQA Dataset</h3>
        <p class="card-text">
          Explore dataset links, live download metrics, language coverage, regional scope, and topic distribution for the multilingual natural QA benchmark.
        </p>
        <div class="landing-actions">
          <a class="btn btn-sm z-depth-0 landing-btn landing-btn--secondary" href="{{ '/resources/multinativqa/' | relative_url }}">Open page</a>
        </div>
      </div>
    </div>
  </div>
  <div class="col-lg-6 mb-4">
    <div class="card h-100 landing-card">
      <div class="card-body">
        <p class="landing-card__kicker">Spoken visual QA</p>
        <h3 class="card-title">EverydayMMQA and OASIS</h3>
        <p class="card-text">
          Explore the multilingual and multimodal framework for culturally grounded spoken visual QA, with the paper summary, pipeline, dataset scale, and benchmark findings in one place.
        </p>
        <div class="landing-actions">
          <a class="btn btn-sm z-depth-0 landing-btn landing-btn--primary" href="{{ '/resources/everydaymmqa/' | relative_url }}">Open page</a>
        </div>
      </div>
    </div>
  </div>
</div>

## NativQA Framework {#framework}


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

<div class="landing-coverage">
  <div class="landing-coverage__chart">
    {% include figure.liquid loading="eager" path="assets/img/data_collection_pipeline_nativqa.png" title="NativQA framework pipeline" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="landing-coverage__content">
    <p>
      The NativQA Framework provides the collection and processing pipeline used to build culturally aligned QA resources from native-speaker and region-aware queries.
    </p>
    <p>
      It supports multilingual dataset construction workflows that can feed both benchmarking and fine-tuning, and it also serves as the foundation for the public resource pages linked above.
    </p>
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
  })();
</script>
