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
		"parent_category" : "123133",
		"title" : "Retro T-Shirt",
		"short_description" : "Quisque sed arcu quis nunc porttitor rutrum faucibus a nunc.",
		"long_description" : "",
		"price" : "25.99",
		"sku" : "898440",
		"weight" : "4.60",
		"stock_number" : "121",
		"title_tag" : "Retro T-Shirt",
		"meta_keywords" : "Tshirt, retro, clothing",
		"meta_description" : "A retro T-shirt",
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
{ "product" : 
	{
		"ID" : "898440",
		"parent_category" : "123133",
		"title" : "Retro T-Shirt",
		"short_description" : "Quisque sed arcu quis nunc porttitor rutrum faucibus a nunc.",
		"long_description" : "",
		"price" : "25.99",
		"sku" : "898440",
		"weight" : "4.60",
		"stock_number" : "121",
		"title_tag" : "Retro T-Shirt",
		"meta_keywords" : "Tshirt, retro, clothing",
		"meta_description" : "A retro T-shirt",
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

* *parent_category* int
* *title* string
* *short_description* string
* *long_description* string
* *price* int
* *sku* int
* *weight* int
* *stock_number* int
* *title_tag* string
* *meta_keywords* string
* *meta_description* string
* *was_price* int
* *rrp* int
* *trade_price* int


### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/products/2455436
{% endhighlight %}

{% highlight javascript %}
{ "product" : 
	{
		"ID" : "898440",
		"parent_category" : "123133",
		"title" : "Retro T-Shirt",
		"short_description" : "Quisque sed arcu quis nunc porttitor rutrum faucibus a nunc.",
		"long_description" : "",
		"price" : "25.99",
		"sku" : "898440",
		"weight" : "4.60",
		"stock_number" : "121",
		"title_tag" : "Retro T-Shirt",
		"meta_keywords" : "Tshirt, retro, clothing",
		"meta_description" : "A retro T-shirt",
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

* *parent_category* int
* *title* string
* *short_description* string
* *long_description* string
* *price* int
* *sku* int
* *weight* int
* *stock_number* int
* *title_tag* string
* *meta_keywords* string
* *meta_description* string
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