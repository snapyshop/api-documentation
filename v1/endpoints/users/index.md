---
layout: nav
title: User Endpoints - SnapyShop REST API Documentation
---

<h1 class="page-header">User Endpoints</h1>

<table class="table table-bordered">
  <tr>
    <td class="request-method"><a href="#get_users">GET</a></td>
    <td><code>/v1/users/:id</code></td>
    <td>Get user by id</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_users_follower">GET</a></td>
    <td><code>/v1/users/followers</code></td>
    <td>Get followers of a user</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_users_followings">GET</a></td>
    <td><code>/v1/users/followings</code></td>
    <td>Get followings of a user</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#put_follow">PUT</a></td>
    <td><code>/v1/users/:id/follow</code></td>
    <td>Follow a user</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#put_unfollow">PUT</a></td>
    <td><code>/v1/users/:id/unfollow</code></td>
    <td>Unfollow a user</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_products">GET</a></td>
    <td><code>/v1/users/:id/products</code></td>
    <td>Get products of a user</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_products_likes">GET</a></td>
    <td><code>/v1/users/:id/products/likes</code></td>
    <td>Get the liked products of a user</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_products_wish_lists">GET</a></td>
    <td><code>/v1/users/:id/products/wish_lists</code></td>
    <td>Get the wishlisted products of a user</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_products_sellings">GET</a></td>
    <td><code>/v1/users/:id/products/sellings</code></td>
    <td>Get the selling products of a user</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#get_products_solds">GET</a></td>
    <td><code>/v1/users/:id/products/solds</code></td>
    <td>Get the sold products of a user</td>
  </tr>
</table>