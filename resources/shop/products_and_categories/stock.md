---
layout: default
title: Stock
---

Stock
=============

*Access Levels*    
__Group:__ shop, products_and_categories   
__Resource:__ stock   
__Version:__ 1  

List stock records for a product
-------------------

{% highlight php %}
GET 	https://api.create.net/products/:product_id/stock
{% endhighlight %}


### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "stock_records" :[ 
	{
		ID : 12345,
		stock_total: 10,
		options: [{
	        ID: 1023305,
	        title: "Colour",
	        items: [{
	            ID: 5039609,
	            title: "Blue",
	        }]
	    }]
	},
	{
		ID : 12346,
		stock_total: 12,
		options: [{
	        ID: 1023305,
	        title: "Colour",
	        items: [{
	            ID: 5039607,
	            title: "Red",
	        }]
	    }],
	}
]}
{% endhighlight %}


Update Stock Level
-------------

{% highlight php %}
PUT 	https://api.create.net/products/:product_id/stock/:stock_record_id
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
			<td>stock_level</td>
			<td>INT</td>
			<td>Required</td>
			<td>What number to update this record's stock level to</td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 200 OK
Location: http://api.create.net/products/2455436/stock/12345
{% endhighlight %}

{% highlight javascript %}
{ stock_record : 
	{
		ID : 12345,
		stock_total: 100,
		options: [{
	        ID: 1023305,
	        title: "Colour",
	        items: [{
	            ID: 5039609,
	            title: "Blue",
	        }]
	    }]
	}
}
{% endhighlight %}

Delete a stock record
-------------

{% highlight php %}
DELETE 	https://api.create.net/products/:product_id/stock/:stock_record_id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}