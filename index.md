---
layout: splash
author_profile: false
header:
  overlay_color: "#1a1a2e"
  overlay_filter: "0.5"
  caption: ""
  actions:
    - label: "🛒 Visit our Shop"
      url: "https://lectronz.com/stores/thebeaverdam"
excerpt: "Engineering open-source hardware, one branch at a time."

feature_row:
  - image_path: /assets/images/designs/MultiBoard.png
    alt: "ESP32 MultiBoard"
    title: "ESP32 MultiBoard"
    excerpt: "A multi connector development board compatible with ESPHome"
    url: /designs/esp32-multiboard/
    btn_label: "Learn More"
    btn_class: "btn--primary"
---

{% include feature_row %}

## All Hardware Designs

<div class="grid__wrapper">
  {% for design in site.designs %}
    {% include archive-single.html post=design type="grid" %}
  {% else %}
    <p><em>No designs published yet. Check back soon!</em></p>
  {% endfor %}
</div>