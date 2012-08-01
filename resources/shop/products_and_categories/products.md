---
layout: default
title: Products
---

Products
=============

*Access Levels*    
__Group:__ shop, products_and_categories
__Resource:__ products

List all products
-------------------

{% highlight php %}
GET 	https://api.create.net/products
{% endhighlight %}

### Input

{% highlight php %}
GET 	https://api.create.net/products?category_id=123133
{% endhighlight %}

* *category_id* int

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "products" :[ 
	{
		"ID" : "898440",
		"parentcat_INC" : "123133",
		"title" : "Retro T-Shirt",
		"shortdesc" : "Quisque sed arcu quis nunc porttitor rutrum faucibus a nunc.",
		"longdesc" : "",
		"price" : "25.99",
		"sku" : "898440",
		"weight" : "4.60",
		"stock_number" : "121",
		"titletag" : "Retro T-Shirt",
		"metakeys" : "Tshirt, retro, clothing",
		"metadesc" : "A retro T-shirt",
		"was_price" : "0.00",
		"rrp" : "0.00",
		"trade_price" : "0.00"
	}
]}
{% endhighlight %}

Get a product
----------

{% highlight php %}
GET 	https://api.create.net/products/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "products" : 
	{
		"ID" : "898440",
		"parentcat_INC" : "123133",
		"title" : "Retro T-Shirt",
		"shortdesc" : "Quisque sed arcu quis nunc porttitor rutrum faucibus a nunc.",
		"longdesc" : "",
		"price" : "25.99",
		"sku" : "898440",
		"weight" : "4.60",
		"stock_number" : "121",
		"titletag" : "Retro T-Shirt",
		"metakeys" : "Tshirt, retro, clothing",
		"metadesc" : "A retro T-shirt",
		"was_price" : "0.00",
		"rrp" : "0.00",
		"trade_price" : "0.00"
	}
}
{% endhighlight %}

Create a product
-------------

{% highlight php %}
POST 	https://api.create.net/products
{% endhighlight %}

### Input

* *parentcat_INC* int
* *title* string
* *shortdesc* string
* *longdesc* string
* *price* int
* *sku* int
* *weight* int
* *stock_number* int
* *titletag* string
* *metakeys* string
* *metadesc* string
* *was_price* int
* *rrp* int
* *trade_price* int


### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/products/2455436
{% endhighlight %}

{% highlight javascript %}
{ "products" : 
	{
		"ID" : "898440",
		"parentcat_INC" : "0",
		"title" : "Retro T-Shirt",
		"shortdesc" : "Quisque sed arcu quis nunc porttitor rutrum faucibus a nunc.",
		"longdesc" : "",
		"price" : "25.99",
		"sku" : "898440",
		"weight" : "4.60",
		"stock_number" : "121",
		"titletag" : "Retro T-Shirt",
		"metakeys" : "Tshirt, retro, clothing",
		"metadesc" : "A retro T-shirt",
		"was_price" : "0.00",
		"rrp" : "0.00",
		"trade_price" : "0.00"
	}
}
{% endhighlight %}

Update a product
-------------

{% highlight php %}
PUT 	https://api.create.net/products/:id
{% endhighlight %}

### Input

* *parentcat_INC* int
* *title* string
* *shortdesc* string
* *longdesc* string
* *price* int
* *sku* int
* *weight* int
* *stock_number* int
* *titletag* string
* *metakeys* string
* *metadesc* string
* *was_price* int
* *rrp* int
* *trade_price* int

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

Delete a product
-------------

{% highlight php %}
DELETE 	https://api.create.net/products/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}