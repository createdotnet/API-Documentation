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
    ID: "4384825",
    order_id: "1948152",
    product_id: "3706871",
    name: "Example Product",
    options: null,
    stock_record_id: null,
    price: "10",
    qty: "1",
    unique_id: "",
    was_price: "0.00",
    trade_price: "7.00"
},
{
    ID: "4384826",
    order_id: "1948152",
    product_id: "3706879",
    name: "Test Product 2",
    options: [{
        ID: 1023305,
        name: "Colour",
        items: [{
            ID: 5039609,
            title: "Blue",
            custom_value: ""
        }]
    }],
    stock_record_id: "442900",
    price: "5",
    qty: "1",
    unique_id: "",
    was_price: "0.00",
    trade_price: "4.00"
}]
{% endhighlight %}
