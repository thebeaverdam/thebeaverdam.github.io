---
layout: home
author_profile: true
header:
  overlay_color: "#333"
  # overlay_image: /assets/images/header-beaver.jpg # Pon la foto cuando la tengas
  caption: "The Beaver Dam: Rugged Hardware for Makers"
excerpt: "Engineering open-source hardware, one branch at a time."
---

## Featured Hardware Designs

<div class="grid__wrapper">
  {% for design in site.designs %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>

[Visit our Shop on Lectronz](https://lectronz.com/stores/thebeaverdam){: .btn .btn--success .btn--large}