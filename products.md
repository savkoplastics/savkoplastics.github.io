---
layout: products
---

<header class="section-header">
  <div class="rte rte--header" style="font-size: 17px;">
    <h2 style="margin-bottom: 20px;">Sewer and Drain</h2>
    <p>
      Our Sewer and Drain Fittings (S&D) are made of two different materials: Polystyrene, available in 3" and 4", meets the ASTM-D 2852 standard; and PVC, available in 4" and 6", meets the ASTM-D 3034 standard. In addition to these standards, we scrutinize every part against our own internal specification to ensure our customers receive only the highest quality products.
    </p>
  </div>
</header>
<hr style="margin: 30px 0">
<div class="grid-uniform">
{% assign products = site.products | map:'product' | sort: 'position' %}
{% for product in products %}
  <div class="grid-item large--one-quarter medium-down--one-half product">
    <a href="/products/{{ product.handle }}" class="product-grid-item product-list-item">
      <div class="grid">
        <div class="grid-item whole">
          <img src="{{ product.images[0] | replace: '.jpg', '_compact.jpg' }}" alt="{{ product.handle }}">
        </div>
        <div class="grid-item whole">
          <p class="h2">{{ product.title }}</p>
        </div>
      </div>
    </a>
  </div>
{% endfor %}
</div>
