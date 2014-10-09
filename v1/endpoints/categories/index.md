---
layout: nav
title: Category Endpoints - SnapyShop REST API Documentation
---

<h1 class="page-header">Category Endpoints</h1>

<table class="table table-bordered">
  <tr>
    <td class="request-method"><a href="#get_categories">GET</a></td>
    <td><code>/categories</code></td>
    <td>Get all snapyshop categories both top and sub level</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_categories_top">GET</a></td>
    <td><code>/categories/tops</code></td>
    <td>Get only top categories</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_categories_sub">GET</a></td>
    <td><code>/categories/subs</code></td>
    <td>Get only sub categories</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_category_id">GET</a></td>
    <td><code>/categories/:id</code></td>
    <td>Get category by id</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_category_parent">GET</a></td>
    <td><code>/categories/:id/parent</code></td>
    <td>Get parent category of a category</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_category_sub_categories">GET</a></td>
    <td><code>/categories/:id/sub_categories</code></td>
    <td>Get sub categories of a category</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_category_products">GET</a></td>
    <td><code>/categories/:id/products</code></td>
    <td>Get products in a category</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_category_products_popular">GET</a></td>
    <td><code>/categories/:id/products/popular</code></td>
    <td>Get popular products in a category</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_category_products_recent">GET</a></td>
    <td><code>/categories/:id/products/recent</code></td>
    <td>Get recent products in a category</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_category_products_search">GET</a></td>
    <td><code>/categories/:id/products/search</code></td>
    <td>Search products in a category</td>
  </tr>
</table>