---
layout: page
title: Publications
permalink: /publications/
---

<h3>Our Group's Work on Pathfinding Benchmarks</h3>

<!-- <h3>2D Benchmarks</h3> -->
{% for publication in site.data.publications %}

{% if publication.group == "2d" %}
{{ publication.author }}, {% if publication.pdf %}<a href="{{ site.baseurl }}/assets/pdf/{{ publication.pdf }}.pdf" target="_blank">{{ publication.title }}</a>, {% else %}{{ publication.title }}, {% endif %}{% if publication.journal %}{{ publication.volume }} _{{ publication.journal }}_ {{ publication.page }} ({{ publication.date }}){% endif %}{% if publication.book %}in _{{ publication.book }}_ ({{ publication.editor }}, {{ publication.date }}){% endif %}{% if publication.institution %}({{ publication.institution }}, {{ publication.date }}){% endif %}&nbsp;<a href="{{ site.url }}{{ site.baseurl }}/2d-benchmarks/"><button class='button syllabus'>2D</button></a>

---
{% endif %}

{% endfor %}

<!-- <h3>Voxel Benchmarks</h3> -->
{% for publication in site.data.publications %}

{% if publication.group == "voxel" %}
{{ publication.author }}, {% if publication.pdf %}<a href="{{ site.baseurl }}/assets/pdf/{{ publication.pdf }}.pdf" target="_blank">{{ publication.title }}</a>, {% else %}{{ publication.title }}, {% endif %}{% if publication.journal %}{{ publication.volume }} _{{ publication.journal }}_ {{ publication.page }} ({{ publication.date }}){% endif %}{% if publication.book %}in _{{ publication.book }}_ ({{ publication.editor }}, {{ publication.date }}){% endif %}{% if publication.institution %}({{ publication.institution }}, {{ publication.date }}){% endif %}&nbsp;<a href="{{ site.url }}{{ site.baseurl }}/3d-benchmarks/voxel-maps/"><button class='button syllabus'>3D</button></a>

---
{% endif %}

{% endfor %}

<!-- <h3>MAPF Benchmarks</h3> -->
{% for publication in site.data.publications %}

{% if publication.group == "mapf" %}
{{ publication.author }}, {% if publication.pdf %}<a href="{{ site.baseurl }}/assets/pdf/{{ publication.pdf }}.pdf" target="_blank">{{ publication.title }}</a>, {% else %}{{ publication.title }}, {% endif %}{% if publication.journal %}{{ publication.volume }} _{{ publication.journal }}_ {{ publication.page }} ({{ publication.date }}){% endif %}{% if publication.book %}in _{{ publication.book }}_ ({{ publication.editor }}, {{ publication.date }}){% endif %}{% if publication.institution %}({{ publication.institution }}, {{ publication.date }}){% endif %}&nbsp;<a href="{{ site.url }}{{ site.baseurl }}/mapf-benchmarks/"><button class='button syllabus'>MAPF</button></a>

---
{% endif %}

{% endfor %}