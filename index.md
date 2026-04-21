---
layout: single
permalink: /
title: ""
author_profile: true
classes: default
---

# Vishnu Tripathi
<p><b>email:</b> vishnu.tripathi.2004@gmail.com</p>

{% if site.data.about.bio %}
{{ site.data.about.bio }}
{% endif %}

---

## Research Interests

{% for item in site.data.about.research_interests %}

<details>
<summary><strong>{{ item.title }}</strong></summary>

<p>{{ item.description }}</p>

</details>

{% endfor %}
---

## Selected Research & Projects

{% for project in site.data.projects.projects %}

<details>
<summary><strong>{{ project.title }}</strong></summary>

<p><em>{{ project.description }}</em></p>

<p><span style="font-weight: 900">Problem:</span> {{ project.problem }}</p>
<p><span style="font-weight: 900">Approach:</span> {{ project.approach }}</p>
<p><span style="font-weight: 900">Contribution:</span> {{ project.contribution }}</p>
<p><span style="font-weight: 900">Insight:</span> {{ project.insight }}</p>

{% if project.links %}
<p>
{% for link in project.links %}
<a href="{{ link.url }}" target="_blank">{{ link.label }}</a>{% unless forloop.last %} | {% endunless %}
{% endfor %}
</p>
{% endif %}

</details>

{% endfor %}

<!-- --- -->



## Publications & Preprints

<!-- <p><em>My work spans LLM evaluation, knowledge-grounded systems, and applied AI, with a focus on understanding model behavior and building reliable real-world AI systems.</em></p> -->

{% for pub in site.data.publications %}

<details>
<summary>
<strong>{{ pub.title }}</strong>
</summary>

<strong>{{ pub.type }}</strong> — <em>{{ pub.venue }} ({{ pub.year }})</em>


<!-- <strong>Authors:</strong> {{ pub.authors }} -->

{% if pub.description %}
<p>{{ pub.description }}</p>
{% endif %}

{% if pub.links %}
<p>
{% for link in pub.links %}
<a href="{{ link.url }}" target="_blank">{{ link.label }}</a>{% unless forloop.last %} | {% endunless %}
{% endfor %}
</p>
{% endif %}

</details>

{% endfor %}

<!-- --- -->


## Other Projects & Engineering Work

<p><em>Additional engineering projects demonstrating system design, deployment, and real-world application of AI systems.</em></p>

{% for project in site.data.other_projects.other_projects %}

<details>
<summary><strong>{{ project.title }}</strong></summary>

<p><em>{{ project.description }}</em></p>

<ul>
{% for item in project.highlights %}
<li>{{ item }}</li>
{% endfor %}
</ul>

{% if project.links %}
<p>
{% for link in project.links %}
<a href="{{ link.url }}" target="_blank">{{ link.label }}</a>{% unless forloop.last %} | {% endunless %}
{% endfor %}
</p>
{% endif %}

</details>

{% endfor %}


## Skills

{% for skill in site.data.skill %}
- {{ skill }}
{% endfor %}