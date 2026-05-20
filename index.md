---
layout: single
permalink: /
title: ""
author_profile: true
classes: default
---

# Vishnu Tripathi
<!-- <p><b>Email:</b> <a href="mailto:vishnu.tripathi.2004@gmail.com">vishnu.tripathi.2004@gmail.com</a></p> -->

<p><a href="mailto:vishnu.tripathi.2004@gmail.com">vishnu.tripathi.2004@gmail.com</a></p>

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
<!-- --- -->


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

<p><em>Workshop papers are labeled explicitly below when they appear in ACL- or COLING-affiliated workshop proceedings.</em></p>

{% for pub in site.data.publications %}

<details>
<summary>
<strong>{{ pub.title }}</strong>
</summary>

<strong>{{ pub.type }}</strong> — <em>{{ pub.venue }} ({{ pub.year }})</em>


<!-- <p style="margin: 0 !important"><strong>Authors:</strong> {{ pub.authors }}</p> -->
<p style="margin: 0 !important">{{ pub.authors }}</p>


{% if pub.description %}
<p style="margin: 0 !important">{{ pub.description }}</p>
{% endif %}

{% if pub.links %}
<p class="pub-links">
{% for link in pub.links %}

<a href="{{ link.url }}" target="_blank" class="btn btn--small pub-links-a">

  {% if link.label == "Paper" %}
    <i class="fas fa-file-alt"></i>

  {% elsif link.label == "Code" %}
    <i class="fab fa-github"></i>

  {% elsif link.label == "PDF" %}
    <i class="fas fa-file-pdf"></i>

  {% elsif link.label == "arXiv" %}
    <i class="ai ai-arxiv"></i>

  {% elsif link.label == "Conference" %}
    <i class="fas fa-chalkboard-teacher"></i>

  {% elsif link.label == "Task" %}
    <i class="fas fa-tasks"></i>

  {% elsif link.label == "Website" %}
    <i class="fas fa-globe"></i>

  {% endif %}

  {{ link.label }}

</a>

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

<!-- --- -->



## Research Experience

{% for exp in site.data.research_experience.experience %}

<details>
<summary><strong>{{ exp.role }}</strong> — <em>{{ exp.lab }}, {{ exp.institution }}</em> &nbsp;|&nbsp; {{ exp.duration }}</summary>

<ul>
{% for item in exp.highlights %}
<li>{{ item }}</li>
{% endfor %}
</ul>

</details>

{% endfor %}


<!-- --- -->



## Skills

{% for group in site.data.skill.skills %}
<div class="skill-group">
  <p class="skill-category">{{ group.category }}</p>
  <p class="skill-items">{{ group.items | join: " &nbsp;·&nbsp; " }}</p>
</div>
{% endfor %}


<!-- --- -->


## Workshops & Academic Service

<!-- **Peer Review** -->

<ul>
{% for r in site.data.workshops.reviewing %}
<li>
{% if r.url and r.url != "" %}
<a href="{{ r.url }}" target="_blank"><strong>{{ r.venue }}</strong></a>
{% else %}
<strong>{{ r.venue }}</strong>
{% endif %}
 — {{ r.role }} ({{ r.details }})
</li>
{% endfor %}
</ul>

<!-- **Conference Service** -->

<ul>
{% for s in site.data.workshops.service %}
<li>
{% if s.url and s.url != "" %}
<a href="{{ s.url }}" target="_blank"><strong>{{ s.event }}</strong></a>
{% else %}
<strong>{{ s.event }}</strong>
{% endif %}
 — {{ s.role }}. {{ s.details }}
</li>
{% endfor %}
</ul>
