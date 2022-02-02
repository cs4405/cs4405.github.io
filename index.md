---
layout: minimal
title: CSE 390HA
nav_exclude: true
seo:
  type: Course
  name: Restorying Computing
---

# {{ site.tagline }}
{: .mb-2 }
{{ site.description }}
{: .fs-6 .fw-300 }

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

In this seminar series, we will engage in the emergent dialogue on critical computing theory by analyzing the politics of computing---the consequences, limitations, and unjust impacts of computing in society. What might a future history of computing look like if computing worked in favor of collective human liberation rather than as *Weapons of Math Destruction*?

{% for module in site.modules %}
{{ module }}
{% endfor %}
