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
    <td class="request-method"><a href="#post_products">POST</a></td>
    <td><code>/products</code></td>
    <td>Create a product</td>
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
    <td class="request-method"><a href="#put_product_id">PUT</a></td>
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
    <td class="request-method"><a href="#post_product_photos">POST</a></td>
    <td><code>/products/:id/photos</code></td>
    <td>Create photo of a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#delete_product_photos">DELETE</a></td>
    <td><code>/products/:id/photos/:photo_id</code></td>
    <td>Delete photo of a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product_likers">GET</a></td>
    <td><code>/products/:id/likers</code></td>
    <td>Get likers of a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#like_product">PUT</a></td>
    <td><code>/products/:id/like</code></td>
    <td>Like a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#unlike_product">PUT</a></td>
    <td><code>/products/:id/unlike</code></td>
    <td>Unike a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_product_wishlisters">GET</a></td>
    <td><code>/products/:id/wish_listers</code></td>
    <td>Get wishlisters of a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#wishlist_product">PUT</a></td>
    <td><code>/products/:id/wish_list</code></td>
    <td>Wishlist a product</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#unwishlist_product">PUT</a></td>
    <td><code>/products/:id/unwish_list</code></td>
    <td>Unwishlist a product</td>
  </tr>
</table>

<h2 class="tags" id="post_products"><code>POST</code> /v1/products</h2>

Create a product. A product must have `category`, `price`, and a `photo`. It responses back `201`, otherwise `400`, `401`, or `500`.

<div class="codehilite">
  <div class="codehilite-header">
    <h4>Request</h4>
  </div>
  <div class="codehilite-body">
{% highlight django%}{% raw %}
http://api.snapyshop.com/v1/products
{% endraw %}{% endhighlight %}
  </div>
  <hr>
  <div class="codehilite-body">
{% highlight json%}{% raw %}
{
  "product": {
    "description": "description",
    "category_id": "540d64c66c69362c72160001",
    "price": 10.0,
    "facebook_account_id": "540d64c66c69362c72160001",
    "facebook_page_id": "540d64c66c69362c72160002",
    "photos": [
      uploaded_file<"10678523_208000989370638_6299764657818101621_n.jpg">
    ]
  }
}
{% endraw %}{% endhighlight %}
  </div>
</div>

<h2 class="tags" id="put_product_id"><code>PUT</code> /v1/products/:id</h2>

Update a product. It responses back `200`, otherwise `400`, `401`, or `500`.

<div class="codehilite">
  <div class="codehilite-header">
    <h4>Request</h4>
  </div>
  <div class="codehilite-body">
{% highlight django%}{% raw %}
http://api.snapyshop.com/v1/products
{% endraw %}{% endhighlight %}
  </div>
  <hr>
  <div class="codehilite-body">
{% highlight json%}{% raw %}
{
  "product": {
    "description": "description",
    "category_id": "540d64c66c69362c72160001",
    "price": 10.0,
    "facebook_account_id": "540d64c66c69362c72160001",
    "facebook_page_id": "540d64c66c69362c72160002",
    "photos": [
      uploaded_file<"10678523_208000989370638_6299764657818101621_n.jpg">
    ]
  }
}
{% endraw %}{% endhighlight %}
  </div>
</div>

<h2 class="tags" id="post_product_photos"><code>POST</code> /v1/products/:id/photos</h2>

Upload a product's photo. It responses back `201`, otherwise `400`, `401`, or `500`.

<div class="codehilite">
  <div class="codehilite-header">
    <h4>Request</h4>
  </div>
  <div class="codehilite-body">
{% highlight django%}{% raw %}
http://api.snapyshop.com/v1/products/:id/photos
{% endraw %}{% endhighlight %}
  </div>
  <hr>
  <div class="codehilite-body">
{% highlight json%}{% raw %}
{
  "product": {
    "photo": uploaded_file<"10678523_208000989370638_6299764657818101621_n.jpg">
  }
}
{% endraw %}{% endhighlight %}
  </div>
</div>

<h2 class="tags" id="post_product_photos"><code>POST</code> /v1/products/:id/photos</h2>

Upload a product's photo. It responses back `201`, otherwise `400`, `401`, or `500`.

<div class="codehilite">
  <div class="codehilite-header">
    <h4>Request</h4>
  </div>
  <div class="codehilite-body">
{% highlight django%}{% raw %}
http://api.snapyshop.com/v1/products/:id/photos
{% endraw %}{% endhighlight %}
  </div>
  <hr>
  <div class="codehilite-body">
{% highlight json%}{% raw %}
{
  "product": {
    "photo": uploaded_file<"10678523_208000989370638_6299764657818101621_n.jpg">
  }
}
{% endraw %}{% endhighlight %}
  </div>
</div>