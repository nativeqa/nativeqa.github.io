---
layout: default
title: events
permalink: /events/
title: events
nav: true
nav_order: 3
pagination:
  enabled: true
  collection: posts
  permalink: /page/:num/
  per_page: 5
  sort_field: date
  sort_reverse: true
  trail:
    before: 1 # The number of links before the current page
    after: 3 # The number of links after the current page
---

<h2>Tutorials</h2>

<ul>
  <li><a href="https://mm-llms-in-the-wild.github.io/">Multilingual and Multimodal LLMs in the Wild: Building for Low-Resource Languages</a> - LREC 2026</li>
  <li><a href="https://llm-low-resource-lang.github.io/">LLMs for Low Resource Languages in Multilingual, Multimodal and Dialectal Settings</a> - EACL 2024</li>
</ul>

<h2>Birds of a Feather (BOF)</h2>

List of events we have organized.

{% include events.liquid %}
