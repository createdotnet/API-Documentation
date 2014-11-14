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
{ "orders" :[
	{
		"ID" : 42050,
		"customer_details" : [
			{
				"ID" : 0,
				"email" : "adam@create.net",
				"first_name" : "Adam",
				"last_name" : "Strawson",
				"company" : "",
				"address1" : "45 Topic Street",
				"address2" : "",
				"address3" : "",
				"city" : "Brighton",
				"county" : "East Sussex",
				"postcode" : "BN1 7TY",
				"country" : "United Kingdom"
				"phone" : "01275 456545"
			}
		],
		"delivery_details" : [
			{
				"first_name" : "Adam",
				"last_name" : "Strawson",
				"company" : "",
				"address1" : "45 Topic Street",
				"address2" : "",
				"address3" : "",
				"city" : "Brighton",
				"county" : "East Sussex",
				"postcode" : "BN1 7TY",
				"country" : "United Kingdom"
				"phone" : "01275 456545",
				"email" : "adam@create.net"
			}
		],
		"date_purchased" : "2012-10-02",
		"order_total" : "25.99",
		"order_currency" : "GBP",
		"shipping_method" : "Standard Postage",
		"shipping_total" : "2.98",
		"tax_total" : "0.00",
		"status" : 2,
		"sub_status" : "",
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
		"ID" : 42050,
		"customer_details" : [
			{
				"ID" : 0,
				"email" : "adam@create.net",
				"first_name" : "Adam",
				"last_name" : "Strawson",
				"company" : "",
				"address1" : "45 Topic Street",
				"address2" : "",
				"address3" : "",
				"city" : "Brighton",
				"county" : "East Sussex",
				"postcode" : "BN1 7TY",
				"country" : "United Kingdom"
				"phone" : "01275 456545"
			}
		],
		"delivery_details" : [
			{
				"first_name" : "Adam",
				"last_name" : "Strawson",
				"company" : "",
				"address1" : "45 Topic Street",
				"address2" : "",
				"address3" : "",
				"city" : "Brighton",
				"county" : "East Sussex",
				"postcode" : "BN1 7TY",
				"country" : "United Kingdom"
				"phone" : "01275 456545",
				"email" : "adam@create.net"
			}
		],
		"date_purchased" : "2012-10-02",
		"order_total" : "25.99",
		"order_currency" : "GBP",
		"shipping_method" : "Standard Postage",
		"shipping_total" : "2.98",
		"tax_total" : "0.00",
		"status" : 2,
		"sub_status" : "",
		"gateway" : "PayPal",
		"gateway_transaction_id" : "3377373820382646",
		"notes" : "",
		"discount_amount" : "",
		"discount_text" : "",
		"referrer" : "smithssweets.co.uk"
	}
}
{% endhighlight %}
