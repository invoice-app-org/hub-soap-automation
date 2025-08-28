---
layout: default
title: SoaP Hub
---

<div class="grid">
{% assign sorted_apps = site.apps | sort: "title" %}
{% for app in sorted_apps %}
  <div class="card">
    <div style="display:flex;justify-content:space-between;align-items:center">
      <h3 style="margin:0"><a href="{{ app.url | relative_url }}">{{ app.title }}</a></h3>
      <span class="badge">{{ app.version | default: "unversioned" }}</span>
    </div>
    {% if app.summary %}<p class="muted">{{ app.summary }}</p>{% endif %}
    {% if app.hero_svg %}
      <a href="{{ app.url | relative_url }}"><img class="diagram" src="{{ app.hero_svg | relative_url }}" alt="diagram of {{ app.title }}"></a>
    {% endif %}
  </div>
{% endfor %}
</div>
