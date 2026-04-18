---
layout: single
permalink: /
title: ""
author_profile: true
classes: default
---

# Vishnu Tripathi

{% if site.data.about.bio %}
{{ site.data.about.bio }}
{% endif %}

---

## Research Interests

{% for item in site.data.about.research_interests %}
- {{ item }}
{% endfor %}

---

## Publications

{% for pub in site.data.publications %}

<details>
<summary>
<strong>{{ pub.title }}</strong> — <em>{{ pub.venue }}</em>
</summary>

<br>

**Authors:** {{ pub.authors }}

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

---

## Selected Research & Projects

{% for project in site.data.projects %}

<details>
<summary>
<strong>{{ project.title }}</strong>
</summary>

<br>

{{ project.description }}

{% if project.tech %}
**Technologies:** {{ project.tech }}
{% endif %}

{% if project.links %}
<p>
{% for link in project.links %}
<a href="{{ link.url }}" target="_blank">{{ link.label }}</a>{% unless forloop.last %} | {% endunless %}
{% endfor %}
</p>
{% endif %}

</details>

{% endfor %}

---

## Skills

{% for skill in site.data.skill %}
- {{ skill }}
{% endfor %}