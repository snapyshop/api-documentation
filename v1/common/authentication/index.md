---
layout: nav
title: Authentication - SnapyShop REST API Documentation
---

<h1 class="page-header">Authentication</h1>

<p class="lead">There two ways to authenticate user:</p>

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
{ "login": "chamnapchhorn@gmail.com", "password": "123456", "client_id": "client_uid", "client_secret": "client_secret" }
{% endraw %}{% endhighlight %}
  </div>
</div>

<div class="codehilite">
  <div class="codehilite-header">
    <h4>Response</h4>
  </div>
  <div class="codehilite-body">
{% highlight json%}{% raw %}
{"access_token":"ee0acd589332541cf47af24cac0809aa9dbc92854ee7f8af3dc817ed5c76965e","token_type":"bearer","expires_in":1209600}
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
{ "facebook_access_token": "CAAImnCxEAV0BAJU1YHA3s298BDgst4xxqHTBIaDelCHUVTqy3DAm7m6BfKiKoQZA0R3G0v2blUYzDx0EUImFqnNHwgJxkZBnzkQK5vSYNJbYMJyjd7furUmZAjD7pict9YnkDIV1tSyPOEZBAXzqSSL3ZB9CRxfxHWAZBfxVMvsripYVxBYFaB", "client_id": "client_uid", "client_secret": "client_secret" }
{% endraw %}{% endhighlight %}
  </div>
</div>

<div class="codehilite">
  <div class="codehilite-header">
    <h4>Response</h4>
  </div>
  <div class="codehilite-body">
{% highlight json%}{% raw %}
{"access_token":"ee0acd589332541cf47af24cac0809aa9dbc92854ee7f8af3dc817ed5c76965e","token_type":"bearer","expires_in":1209600}
{% endraw %}{% endhighlight %}
  </div>
</div>