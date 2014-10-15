---
layout: nav
title: Endpoints - SnapyShop REST API Documentation
---

<h1 class="page-header">Endpoints</h1>
Once you've registered your client it's easy to start requesting data from SnapyShop.

Every request made to SnapyShop REST API must provide authentication. API users must send with params `access_token` as query string.

`access_token` will be expired in a week.

<div class="codehilite">
  <div class="codehilite-body">
{% highlight django%}{% raw %}
http://api.snapyshop.com/v1/products?access_token=ACCESS-TOKEN
{% endraw %}{% endhighlight %}
  </div>
</div>