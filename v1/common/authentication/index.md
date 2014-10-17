---
layout: nav
title: Authentication - SnapyShop REST API Documentation
---

<h1 class="page-header">Authentication</h1>

<table class="table table-bordered">
  <tr>
    <td class="request-method"><a href="#login_and_password">POST</a></td>
    <td><code>/v1/oauth/token</code></td>
    <td>Returns the access_token for password user</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#facebook">POST</a></td>
    <td><code>/v1/oauth/token/facebook</code></td>
    <td>Returns the access_token for facebook user</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#revoke_token">POST</a></td>
    <td><code>/v1/oauth/revoke</code></td>
    <td>Revoke the given access_token</td>
  </tr>
  <tr>
    <td class="request-method"><a href="#token_info">GET</a></td>
    <td><code>/v1/oauth/token/info</code></td>
    <td>Returns the access_token information</td>
  </tr>
</table>

<h2 class="tags" id="login_and_password"><code>POST</code> /v1/oauth/token</h2>

Authenticate user with `login` and `password`. It returns `access_token` back if successful, otherwise returns `401`.

<div class="codehilite">
  <div class="codehilite-header">
    <h4>Request</h4>
  </div>
  <div class="codehilite-body">
{% highlight django%}{% raw %}
http://api.snapyshop.com/v1/oauth/token
{% endraw %}{% endhighlight %}
  </div>
  <hr>
  <div class="codehilite-body">
{% highlight json%}{% raw %}
{
  "login": "chamnapchhorn@gmail.com",
  "password": "123456",
  "client_id": "client_uid",
  "client_secret": "client_secret"
}
{% endraw %}{% endhighlight %}
  </div>
</div>

<div class="codehilite">
  <div class="codehilite-header">
    <h4>Response</h4>
  </div>
  <div class="codehilite-body">
{% highlight json%}{% raw %}
{
  "access_token": "ee0acd589332541cf47af24cac0809aa9dbc92854ee7f8af3dc817ed5c76965e",
  "token_type": "bearer",
  "expires_in": 1209600
}
{% endraw %}{% endhighlight %}
  </div>
</div>

<h2 class="tags" id="facebook"><code>POST</code> /v1/oauth/token/facebook</h2>

Authenticate user with `facebook_access_token`. It will sign up if this user doesn't exist in SnapyShop. It returns `access_token` back if successful, otherwise returns `401`.

<div class="codehilite">
  <div class="codehilite-header">
    <h4>Request</h4>
  </div>
  <div class="codehilite-body">
{% highlight django%}{% raw %}
http://api.snapyshop.com/v1/oauth/token/facebook
{% endraw %}{% endhighlight %}
  </div>
  <hr>
  <div class="codehilite-body">
{% highlight json%}{% raw %}
{
  "facebook_access_token": "CAAImnCxEAV0BAJU1YHA3s298BDgst4xxqHTBIaDelCHUVTqy3DAm7m6BfKiKoQZA0R3G0v2blUYzDx0EUImFqnNHwgJxkZBnzkQK5vSYNJbYMJyjd7furUmZAjD7pict9YnkDIV1tSyPOEZBAXzqSSL3ZB9CRxfxHWAZBfxVMvsripYVxBYFaB",
  "client_id": "client_uid",
  "client_secret": "client_secret"
}
{% endraw %}{% endhighlight %}
  </div>
</div>

<div class="codehilite">
  <div class="codehilite-header">
    <h4>Response</h4>
  </div>
  <div class="codehilite-body">
{% highlight json%}{% raw %}
{
  "access_token": "ee0acd589332541cf47af24cac0809aa9dbc92854ee7f8af3dc817ed5c76965e",
  "token_type": "bearer",
  "expires_in": 1209600
}
{% endraw %}{% endhighlight %}
  </div>
</div>

<h2 class="tags" id="revoke_token"><code>POST</code> /v1/oauth/revoke</h2>

Revoke the given `access_token`, otherwise returns `401`. It can be used to implement log out.

<div class="codehilite">
  <div class="codehilite-header">
    <h4>Request</h4>
  </div>
  <div class="codehilite-body">
{% highlight django%}{% raw %}
http://api.snapyshop.com/v1/oauth/revoke?access_token=b246007424251b119023c6b897f7a3b49f1a1168fec4a75dced6b2b2cd30d82d
{% endraw %}{% endhighlight %}
  </div>
</div>

<h2 class="tags" id="token_info"><code>GET</code> /v1/oauth/token/info</h2>

Return information about `access_token`, otherwise returns `401`.

<div class="codehilite">
  <div class="codehilite-header">
    <h4>Request</h4>
  </div>
  <div class="codehilite-body">
{% highlight django%}{% raw %}
http://api.snapyshop.com/v1/oauth/token/info?access_token=b246007424251b119023c6b897f7a3b49f1a1168fec4a75dced6b2b2cd30d82d
{% endraw %}{% endhighlight %}
  </div>
</div>

<div class="codehilite">
  <div class="codehilite-header">
    <h4>Response</h4>
  </div>
  <div class="codehilite-body">
{% highlight json%}{% raw %}
{
  "data": {
    "id": "543ff176436861b78d000000",
    "token": "b246007424251b119023c6b897f7a3b49f1a1168fec4a75dced6b2b2cd30d82d",
    "expires_in": null,
    "revoked_at": null,
    "user": {
      "id": "543ff13d436861b3f82e0000",
      "name": "Chamnap Chhorn"
    },
    "application": {
      "id": "543ff19a436861b240000000",
      "name": "Android"
    },
    "created_at": "2014-10-16T16:26:22.099Z",
    "updated_at": "2014-10-16T16:26:22.099Z"
  }
}
{% endraw %}{% endhighlight %}
  </div>
</div>