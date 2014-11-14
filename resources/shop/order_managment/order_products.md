---
layout: default
title: Order Products
---

Order Products
=============

*Access Levels*    
__Group:__ shop, order_managment     
__Resource:__ order_products

List all products in an order
-------------------

{% highlight php %}
GET 	https://api.create.net/orders/{order_id}/products
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
[{
    "ID": "2096864",
    "order_id": "1693218",
    "product_id": "1718379",
    "name": "blah test",
    "options": "",
    "stock_record_id": null,
    "price": "0.5",
    "qty": "1",
    "unique_id": "",
    "was_price": "0.00",
    "trade_price": null
}, {
    "ID": "3752220",
    "order_id": "1693218",
    "product_id": "3219995",
    "name": "Cardboard Box",
    "options": "",
    "stock_record_id": null,
    "price": "1.5",
    "qty": "2",
    "unique_id": "",
    "was_price": "0.00",
    "trade_price": null
}]	
{% endhighlight %}
