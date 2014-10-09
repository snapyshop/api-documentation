---
layout: nav
title: Product Endpoints - SnapyShop REST API Documentation
---

<h1 class="page-header">Product Endpoints</h1>

<table class="table table-bordered">
  <tr>
    <td class="request-method"><a href="#get_products">GET</a></td>
    <td><code>/products</code></td>
    <td>Get all snapyshop products</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_products_popular">GET</a></td>
    <td><code>/products/popular</code></td>
    <td>Get all popular products</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_products_recent">GET</a></td>
    <td><code>/products/recent</code></td>
    <td>Get all recent products</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product_id">GET</a></td>
    <td><code>/products/:id</code></td>
    <td>Get product by id</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product_id">PUT</a></td>
    <td><code>/products/:id</code></td>
    <td>Update product information by id</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product">DELETE</a></td>
    <td><code>/products/:id</code></td>
    <td>Delete a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product">PUT</a></td>
    <td><code>/products/:id/sold</code></td>
    <td>Sold a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product">PUT</a></td>
    <td><code>/products/:id/complete</code></td>
    <td>Mark a product as complete</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product_photos">GET</a></td>
    <td><code>/products/:id/photos</code></td>
    <td>Get photos of a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_products_sub_products">POST</a></td>
    <td><code>/products/:id/photos</code></td>
    <td>Create photo of a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product">DELETE</a></td>
    <td><code>/products/:id/photos/:photo_id</code></td>
    <td>Delete photo of a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product">GET</a></td>
    <td><code>/products/:id/likers</code></td>
    <td>Get likers of a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product">PUT</a></td>
    <td><code>/products/:id/like</code></td>
    <td>Like a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product">PUT</a></td>
    <td><code>/products/:id/unlike</code></td>
    <td>Unike a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product">GET</a></td>
    <td><code>/products/:id/wish_listers</code></td>
    <td>Get wishlisters of a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product">PUT</a></td>
    <td><code>/products/:id/wish_list</code></td>
    <td>Wishlist a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product">PUT</a></td>
    <td><code>/products/:id/unwish_list</code></td>
    <td>Unwishlist a product</td>
  </tr>
</table>