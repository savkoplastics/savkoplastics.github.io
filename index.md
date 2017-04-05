---
layout: default
---

<div class="grid-uniform">

{% for product in site.data.mapped_products %}
  <div class="grid-item large--one-quarter medium-down--one-half product">
    <a href="/products/{{ product.handle }}" class="product-grid-item product-list-item">
      <div class="grid">
        <div class="grid-item whole">
          <img src="{{ product.images[0] }}" alt="{{ product.handle }}" height="160" width="160">
          <!-- make image compact CDN size & include alt tag with encoding -->
        </div>
        <div class="grid-item four-fifths">
          <p class="h3">{{ product.title }}</p>
        </div>
      </div>
    </a>
  </div>
{% endfor %}
</div>
