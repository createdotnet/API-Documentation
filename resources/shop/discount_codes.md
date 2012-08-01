---
layout: default
title: Discount Codes
---

Discount Codes
=============

*Access Levels*    
__Group:__ shop
__Resource:__ discount_codes

List all discount codes
-----------------------

{% highlight php %}
GET 	https://api.create.net/discount_codes
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "discount_codes" :[ 
	{
		"ID" : "5890",
		"name" : "Facebook Friends Discount",
		"code" : "FBF010",
		"type" : "percent",
		"amount" : "10.00",
		"expiry" : "0000-00-00"
	}
]}
{% endhighlight %}

Get a discount code
-------------------

{% highlight php %}
GET 	https://api.create.net/discount_codes/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "discount_codes" : 
	{
		"ID" : "5890",
		"name" : "Facebook Friends Discount",
		"code" : "FBF010",
		"type" : "percent",
		"amount" : "10.00",
		"expiry" : "0000-00-00"
	}
}
{% endhighlight %}

Create a discount code
----------------------

{% highlight php %}
POST 	https://api.create.net/discount_codes
{% endhighlight %}

### Input

* *name* string
* *code* string
* *type* percent, amount
* *amount* int
* *expiry* date

### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/discount_codes/5890
{% endhighlight %}

{% highlight javascript %}
{ "discount_codes" : 
	{
		"ID" : "5890",
		"name" : "Facebook Friends Discount",
		"code" : "FBF010",
		"type" : "percent",
		"amount" : "10.00",
		"expiry" : "0000-00-00"
	}
}
{% endhighlight %}

Update a discount code
----------------------

{% highlight php %}
PUT 	https://api.create.net/discount_codes/:id
{% endhighlight %}

### Input

* *name* string
* *code* string
* *type* percent, amount
* *amount* int
* *expiry* date

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

Delete a discount code
----------------------

{% highlight php %}
DELETE 	https://api.create.net/discount_codes/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}