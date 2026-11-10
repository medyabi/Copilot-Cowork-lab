---
title: Online Hosted Instructions
permalink: index.html
layout: default
---

# Content Directory

Hyperlinks to each of the lab exercises and their teaching editions are listed below.

The lab files used in the labs are in the [`Allfiles`](https://github.com/{{ site.github.repository_nwo }}/tree/main/Allfiles) folder. You can [download the whole repository as a ZIP]({{ site.github.zip_url }}).

> **Note:** Copilot Cowork is AI-powered, so your results will differ from the screenshots. Follow the workflow and the expected outcome rather than the exact wording.

## Labs

{% assign labs = site.pages | where_exp: "p", "p.lab" | sort: "url" %}
| Module | Lab |
| --- | --- |
{% for activity in labs %}| {{ activity.lab.module }} | [{{ activity.lab.title }}]({{ site.baseurl }}{{ activity.url }}) |
{% endfor %}

## Teaching editions

Each lab, explained step by step in a simple, conversational style: why each step matters, not just what to click.

{% assign teaching = site.pages | where_exp: "p", "p.teaching" | sort: "url" %}
| Module | Teaching edition |
| --- | --- |
{% for activity in teaching %}| {{ activity.teaching.module }} | [{{ activity.teaching.title }}]({{ site.baseurl }}{{ activity.url }}) |
{% endfor %}

## For trainers

- [Trainer Guide]({{ site.baseurl }}/Instructions/Trainer/Trainer-Guide.html): workshop overview, lab map, prerequisites, pre-flight checklist and delivery notes for every lab.
