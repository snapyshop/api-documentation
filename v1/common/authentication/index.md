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
    <td class="request-method"><a href="#refresh_token">POST</a></td>
    <td><code>/v1/oauth/token</code></td>
    <td>Refresh the access token</td>
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
  "grant_type": "password",
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
  "refresh_token":"5374dc43d84c2ff085457abe6dc440ef14259c3ba293fbeaae810e2809f74357",
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
  "access_token": "51f1ec0ea5912032f22759358c5c969d07df1a47d123052baf700922cea50335",
  "token_type": "bearer",
  "expires_in": 5184000,
  "refresh_token": "0d117b817aeac27efb3bafdc4d2fb851fda3c0e7f086c67daf74d8d0ecbdf137"
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

<h2 class="tags" id="refresh_token"><code>POST</code> /v1/oauth/token</h2>

Refresh the `access_token`, otherwise returns `401`. You can only refresh the `access_token` before it's expired or it's not revoked. `access_token` will be expired in two months.

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
  "refresh_token": "157e9e6bac8abbdf1ccaeaddf972bdfc7a18662f0abd7ec636a7b374e3daa803",
  "client_id": "client_uid",
  "client_secret": "secret",
  "grant_type": "refresh_token"
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
  "access_token": "658958a50cfdd81f76fc0afb316b3f25b3c4098e7c8a83d2952858e55bd3d1ed",
  "token_type": "bearer",
  "expires_in": 5184000,
  "refresh_token": "9bee5d478a2834803c5e3fc9f8ab9dfa1426e0beaf765df4527730e57105481f"
}
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
    "id": "54414a184368613f6b010000",
    "token": "157e9e6bac8abbdf1ccaeaddf972bdfc7a18662f0abd7ec636a7b374e3daa803",
    "refresh_token": "8d80ecc3e044d008eb27511016768b298409cee26464acf81df76b97d4ee6204",
    "expires_in": 5184000,
    "expired_at": "2014-12-16T16:55:52.263Z",
    "revoked_at": null,
    "user": {
      "id": "543ff13d436861b3f82e0000",
      "name": "Chamnap Chhorn"
    },
    "application": {
      "id": "543ff19a436861b240000000",
      "name": "Android"
    },
    "created_at": "2014-10-17T16:55:52.263Z",
    "updated_at": "2014-10-17T16:55:52.263Z"
  }
}
{% endraw %}{% endhighlight %}
  </div>
</div>