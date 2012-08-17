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
		"ID" : 5890,
		"name" : "Facebook Friends Discount",
		"code" : "FBF010",
		"type" : "percent",
		"amount" : "10.00",
		"expiry" : "9999-99-99"
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
{ "discount_code" : 
	{
		"ID" : 5890,
		"name" : "Facebook Friends Discount",
		"code" : "FBF010",
		"type" : "percent",
		"amount" : "10.00",
		"expiry" : "9999-99-99"
	}
}
{% endhighlight %}

Create a discount code
----------------------

{% highlight php %}
POST 	https://api.create.net/discount_codes
{% endhighlight %}

### Input

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
			<td>name</td>
			<td>string</td>
			<td>Required</td>
			<td>The name of the discount code</td>
		</tr>
		<tr>
			<td>code</td>
			<td>string</td>
			<td>Required</td>
			<td>The discount code <br /><small>Letters and/or numbers only</small></td>
		</tr>
		<tr>
			<td>type</td>
			<td>string</td>
			<td>Required</td>
			<td>The type of discount code <br /><small>Options: percent, amount</small></td>
		</tr>
		<tr>
			<td>amount</td>
			<td>string</td>
			<td>Required</td>
			<td>The discount amount</td>
		</tr>
		<tr>
			<td>expiry</td>
			<td>date</td>
			<td>Required</td>
			<td>The date to expire <br /><small>yyyy-mm-dd OR 9999-99-99 to never expire</small></td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/discount_codes/5890
{% endhighlight %}

{% highlight javascript %}
{ "discount_code" : 
	{
		"ID" : 5890,
		"name" : "Facebook Friends Discount",
		"code" : "FBF010",
		"type" : "percent",
		"amount" : "10.00",
		"expiry" : "9999-99-99"
	}
}
{% endhighlight %}

Update a discount code
----------------------

{% highlight php %}
PUT 	https://api.create.net/discount_codes/:id
{% endhighlight %}

### Input

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
			<td>name</td>
			<td>string</td>
			<td>Optional</td>
			<td>The name of the discount code</td>
		</tr>
		<tr>
			<td>code</td>
			<td>string</td>
			<td>Optional</td>
			<td>The discount code <br /><small>Letters and/or numbers only</small></td>
		</tr>
		<tr>
			<td>type</td>
			<td>string</td>
			<td>Optional</td>
			<td>The type of discount code <br /><small>Options: percent, amount</small></td>
		</tr>
		<tr>
			<td>amount</td>
			<td>string</td>
			<td>Optional</td>
			<td>The discount amount</td>
		</tr>
		<tr>
			<td>expiry</td>
			<td>date</td>
			<td>Optional</td>
			<td>The date to expire <br /><small>yyyy-mm-dd OR 9999-99-99 to never expire</small></td>
		</tr>
	</tbody>
</table>

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