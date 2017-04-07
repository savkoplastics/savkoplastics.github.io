---
layout: default
---

<header class="section-header">
  <h1>Manufacturing</h1>
  <div class="rte rte--header" style="font-size: 15px">
    For over 50 years we have been manufacturing plastic pipe and fittings. Our Sewer and Drain Fittings<span> (S&amp;D)</span> are made of two different materials. Polystyrene, available in 3" and 4" meets the ASTM-D 2852 Standard. We also have PVC, available in 4" and 6" which meets the ASTM-D 3034 Standard.
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
