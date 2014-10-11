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

<table>
	<thead>
		<tr>
			<th>Param</th>
			<th>Type</th>
			<th>Required</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>date\_purchased__from</td>
			<td>datetime</td>
			<td>Optional</td>
			<td>Orders after a certain date <br /><small>yyyy-mm-dd hh:mm:ss</small></td>
		</tr>
		<tr>
			<td>date\_purchased__to</td>
			<td>datetime</td>
			<td>Optional</td>
			<td>Orders up to a certain date <br /><small>yyyy-mm-dd hh:mm:ss</small></td>
		</tr>
		<tr>
			<td>status</td>
			<td>INT</td>
			<td>Optional</td>
			<td>Get orders by status <br /><small>1 = X, 2 = X etc</small></td>
		</tr>
		<tr>
			<td>customer_id</td>
			<td>INT</td>
			<td>Optional</td>
			<td>Get orders from a single customer</td>
		</tr>
	</tbody>
</table>

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
