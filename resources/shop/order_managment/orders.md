---
layout: default
title: Orders
---

Orders
=============

*Access Levels*    
__Group:__ shop, order_managment     
__Resource:__ orders

List all orders
-------------------

{% highlight php %}
GET 	https://api.create.net/orders
{% endhighlight %}

### Input

{% highlight php %}
GET 	https://api.create.net/orders?datetime_from=2010-04-07%2018:08:14
{% endhighlight %}
* *datetime_from* datetime
* *datetime_to* datetime
* *status* int
* *customer_id* int

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "orders" :[
	{
		"ID" : "42050",
		"customer_id" : "0",
		"customer_email" : "adam@create.net",
		"customer_firstname" : "Adam",
		"customer_lastname" : "Strawson",
		"customer_company" : "",
		"customer_address1" : "45 Topic Street",
		"customer_address2" : "",
		"customer_address3" : "",
		"customer_city" : "Brighton",
		"customer_county" : "East Sussex",
		"customer_postcode" : "BN1 7TY",
		"customer_country" : "United Kingdom"
		"customer_phone" : "01275 456545",
		"delivery_firstname" : "Adam",
		"delivery_lastname" : "Strawson",
		"delivery_company" : "",
		"delivery_address1" : "45 Topic Street",
		"delivery_address2" : "",
		"delivery_address3" : "",
		"delivery_city" : "Brighton",
		"delivery_county" : "East Sussex",
		"delivery_postcode" : "BN1 7TY",
		"delivery_country" : "United Kingdom"
		"delivery_phone" : "01275 456545",
		"delivery_email" : "adam@create.net",
		"date_purchased" : "2012-10-02",
		"order_total" : "25.99",
		"order_currency" : "GBP",
		"shipping_method" : "Standard Postage",
		"shipping_total" : "2.98",
		"tax_total" : "0.00",
		"status" : "2",
		"substatus" : "",
		"gateway" : "PayPal",
		"gateway_transaction_id" : "3377373820382646",
		"notes" : "",
		"discount_amount" : "",
		"discount_text" : "",
		"referrer" : "smithssweets.co.uk"
	}
]}
{% endhighlight %}

Get a single orders
-------------------------

{% highlight php %}
GET 	https://api.create.net/orders/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "order" :
	{
		"ID" : "42050",
		"customer_id" : "0",
		"customer_email" : "adam@create.net",
		"customer_firstname" : "Adam",
		"customer_lastname" : "Strawson",
		"customer_company" : "",
		"customer_address1" : "45 Topic Street",
		"customer_address2" : "",
		"customer_address3" : "",
		"customer_city" : "Brighton",
		"customer_county" : "East Sussex",
		"customer_postcode" : "BN1 7TY",
		"customer_country" : "United Kingdom"
		"customer_phone" : "01275 456545",
		"delivery_firstname" : "Adam",
		"delivery_lastname" : "Strawson",
		"delivery_company" : "",
		"delivery_address1" : "45 Topic Street",
		"delivery_address2" : "",
		"delivery_address3" : "",
		"delivery_city" : "Brighton",
		"delivery_county" : "East Sussex",
		"delivery_postcode" : "BN1 7TY",
		"delivery_country" : "United Kingdom"
		"delivery_phone" : "01275 456545",
		"delivery_email" : "adam@create.net",
		"date_purchased" : "2012-10-02",
		"order_total" : "25.99",
		"order_currency" : "GBP",
		"shipping_method" : "Standard Postage",
		"shipping_total" : "2.98",
		"tax_total" : "0.00",
		"status" : "2",
		"substatus" : "",
		"gateway" : "PayPal",
		"gateway_transaction_id" : "3377373820382646",
		"notes" : "",
		"discount_amount" : "",
		"discount_text" : "",
		"referrer" : "smithssweets.co.uk"
	}
}
{% endhighlight %}