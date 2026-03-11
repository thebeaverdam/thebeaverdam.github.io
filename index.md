---
layout: splash
author_profile: false
header:
  overlay_color: "#1a1a2e"
  overlay_filter: "0.5"
  caption: "The Beaver Dam: Rugged Hardware for Makers"
  actions:
    - label: "🛒 Visit our Shop"
      url: "https://lectronz.com/stores/thebeaverdam"
excerpt: "Engineering open-source hardware, one branch at a time."

feature_row:
  - image_path: /assets/images/designs/MultiBoard.png
    alt: "ESP32 MultiBoard v1.1"
    title: "ESP32 MultiBoard v1.1"
    excerpt: "A rugged IoT development board with ESP32-S3, 8MB PSRAM, LiPo + Solar power."
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