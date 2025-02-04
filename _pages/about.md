---
layout: about
title: about
permalink: /
subtitle: "NativQA: Multilingual Culturally-Aligned Natural Query for LLMs"

#profile:
#  align: center
#  image: language_donut_chart.png
#  image_circular: false
  # crops the image to make it circular
news: true # includes a list of news items
selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page
---

Natural Question Answering (QA) datasets play a crucial role in evaluating the capabilities of large language models (LLMs), ensuring their effectiveness in real-world applications. Despite the numerous QA datasets that have been developed, there is a notable lack of region-specific datasets created by native users in their own languages. This gap hinders the effective benchmarking of LLMs for regional and cultural specificities and limits the development of fine-tuned models.

In this study, we propose a scalable, language-independent framework, NativQA, to seamlessly construct culturally and regionally aligned QA datasets in native languages for LLM evaluation and tuning. We demonstrate the efficacy of the proposed framework by designing a multilingual natural QA dataset, MultiNativQA, consisting of approximately 64k manually annotated QA pairs in seven languages, ranging from high- to extremely low-resource languages, based on queries from native speakers from nine regions covering 18 topics.

We benchmark both open- and closed-source LLMs using the MultiNativQA dataset. Additionally, we showcase the framework's efficacy in constructing fine-tuning data, especially for low-resource and dialectally rich languages. Both the NativQA framework and the MultiNativQA dataset have been made publicly available to the community.

<br/>
<br/>
{% include figure.liquid loading="eager" path="assets/img/data_collection_pipeline_nativqa.png" title="example image" class="img-fluid rounded z-depth-1" %}

<br/>
<br/>

#### Multi*NativQA* Dataset

##### Statistics

<div style="width: 50%; height: auto; margin: 0 auto;">
    {% include figure.liquid loading="eager" path="assets/img/language_donut_chart.png" title="example image" class="img-fluid rounded z-depth-1" %}
</div>


##### Topics Coverage

| **Selected topics used as seed to collect manual queries.**                                                                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Animal, Business, Cloth, Education, Events, Food & Drinks, General, Geography, Immigration Related, Language, Literature, Names & Persons, Plants, Religion, Sports & Games, Tradition, Travel, Weather |

<br/>
##### Language Coverage
Arabic, Assamese, Bangla, English, Hindi, Nepali, Turkish
