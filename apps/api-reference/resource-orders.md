---
layout: page
key: api-resources-orders
title: Orders
---

A request by a customer to purchase one or more products from a shop.
An order is created as soon as a customer completes the checkout process.
Depending on the shop settings, the order will be created before or after the payment process.

<ul id="resource-list">
  {% for page in site.pages %}
    {% assign match = page.key | regex_match: '^apps-api-([a-z]+)-shops-shopid-orders(.*)-information$' %}
    {% if match %}
      <li class="resource-entry">
        <span class="http-method http-method-{{ page.raml_method.method | downcase }}">{{ page.raml_method.method }}</span>
        <a href="{{ page.url | prepend: site.baseurl }}">{{ page.raml_resource.relative_uri }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>
