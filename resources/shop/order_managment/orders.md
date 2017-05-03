---
layout: default
title: Orders
---

Orders
=============

*Access Levels*    
__Group:__ shop, order_managment     
__Resource:__ orders

### Order statuses
These endpoints use the following values to represent the status of an order:

 - `status` 1 - Pending
 
   - `sub_status` 1 - Waiting Payment
   
 - `status` 2 - Processing
 
   - `sub_status` 1 - Picking
   
   - `sub_status` 2 - Packaging
   
   - `sub_status` 3 - Waiting Dispatch
   
 - `status` 3 - Dispatched
 
 - `status` 4 - Refunded
 
 - `status` 5 - Cancelled
 

List all orders
-------------------

{% highlight php %}
GET 	https://api.create.net/orders
{% endhighlight %}

### Input

{% highlight php %}
GET 	https://api.create.net/orders?date_purchased__from=2010-04-07%2018:08:14
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
			<td>date_purchased__from</td>
			<td>datetime</td>
			<td>Optional</td>
			<td>Orders after a certain date <br /><small>yyyy-mm-dd hh:mm:ss</small></td>
		</tr>
		<tr>
			<td>date_purchased__to</td>
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
				"email" : "name@example.com",
				"first_name" : "John",
				"last_name" : "Doe",
				"company" : "",
				"address1" : "45 Topic Street",
				"address2" : "",
				"address3" : "",
				"city" : "Brighton",
				"county" : "East Sussex",
				"postcode" : "BN1 7TY",
				"country" : "United Kingdom"
				"phone" : "01234 567890"
			}
		],
		"delivery_details" : [
			{
				"first_name" : "John",
				"last_name" : "Doe",
				"company" : "",
				"address1" : "45 Topic Street",
				"address2" : "",
				"address3" : "",
				"city" : "Brighton",
				"county" : "East Sussex",
				"postcode" : "BN1 7TY",
				"country" : "United Kingdom"
				"phone" : "01234 567890",
				"email" : "name@example.com"
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

Get a single order
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
				"email" : "name@example.com",
				"first_name" : "John",
				"last_name" : "Doe",
				"company" : "",
				"address1" : "45 Topic Street",
				"address2" : "",
				"address3" : "",
				"city" : "Brighton",
				"county" : "East Sussex",
				"postcode" : "BN1 7TY",
				"country" : "United Kingdom"
				"phone" : "01234 567890"
			}
		],
		"delivery_details" : [
			{
				"first_name" : "John",
				"last_name" : "Doe",
				"company" : "",
				"address1" : "45 Topic Street",
				"address2" : "",
				"address3" : "",
				"city" : "Brighton",
				"county" : "East Sussex",
				"postcode" : "BN1 7TY",
				"country" : "United Kingdom"
				"phone" : "01234 567890",
				"email" : "name@example.com"
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

Update an order
-------------------------

{% highlight php %}
PUT 	https://api.create.net/orders/:id
{% endhighlight %}

### Input
The request can either be sent as a form post or JSON. The structure is the same as a single order and all fields are optional

{% highlight javascript %}
{
	"customer_details" : [
		{
			"ID" : 0,
			"email" : "name@example.com",
			"first_name" : "John",
			"last_name" : "Doe",
			"company" : "",
			"address1" : "45 Road Street",
			"address2" : "",
			"address3" : "",
			"city" : "Brighton",
			"county" : "East Sussex",
			"postcode" : "BN1 7TY",
			"country" : "United Kingdom"
			"phone" : "01234 567890"
		}
	],
	"delivery_details" : [
		{
			"first_name" : "John",
			"last_name" : "Doe",
			"company" : "",
			"address1" : "45 Road Street",
			"address2" : "",
			"address3" : "",
			"city" : "Brighton",
			"county" : "East Sussex",
			"postcode" : "BN1 7TY",
			"country" : "United Kingdom"
			"phone" : "01234 567890",
			"email" : "name@example.com"
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
	"referrer" : ""
}
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

