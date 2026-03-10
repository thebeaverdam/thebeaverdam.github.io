---
layout: archive
author_profile: true
header:
  overlay_color: "#333"
  caption: "The Beaver Dam: Rugged Hardware for Makers"
excerpt: "Engineering open-source hardware, one branch at a time."
---

## Featured Hardware Designs

<div class="grid__wrapper">
  {% assign designs = site.designs | default: site.collections.designs.docs %}
  {% for design in designs %}
    {% include archive-single.html post=design type="grid" %}
  {% else %}
    <p>No designs found. Check if the collection is correctly configured in _config.yml and the folder _designs contains .md files.</p>
  {% endfor %}
</div>

[Visit our Shop on Lectronz](https://lectronz.com/stores/thebeaverdam){: .btn .btn--success .btn--large}