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
			<td>category_id</td>
			<td>INT</td>
			<td>Optional</td>
			<td>Get all products from a single category</td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "products" :[ 
	{
		"ID" : 898440,
		"parent_category" : 123133,
		"title" : "Retro T-Shirt",
		"short_description" : "Quisque sed arcu quis nunc porttitor rutrum faucibus a nunc.",
		"long_description" : "",
		"price" : "25.99",
		"sku" : "898440",
		"weight" : "4.60",
		"stock_number" : 121,
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
		"ID" : 898440,
		"parent_category" : 123133,
		"title" : "Retro T-Shirt",
		"short_description" : "Quisque sed arcu quis nunc porttitor rutrum faucibus a nunc.",
		"long_description" : "",
		"price" : "25.99",
		"sku" : "898440",
		"weight" : "4.60",
		"stock_number" : 121,
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
			<td>parent_category</td>
			<td>INT</td>
			<td>Optional</td>
			<td>The ID of the category <br /><small>See: <a href="http://createdotnet.github.com/API-Documentation/resources/shop/products_and_categories/categories.html">Categories</a></small></td>
		</tr>
		<tr>
			<td>title</td>
			<td>string</td>
			<td>Required</td>
			<td>The product title</td>
		</tr>
		<tr>
			<td>short_description</td>
			<td>string</td>
			<td>Optional</td>
			<td>The product short description</td>
		</tr>
		<tr>
			<td>long_description</td>
			<td>string</td>
			<td>Optional</td>
			<td>The product long description</td>
		</tr>
		<tr>
			<td>price</td>
			<td>INT</td>
			<td>Required</td>
			<td>The product price</td>
		</tr>
		<tr>
			<td>sku</td>
			<td>string</td>
			<td>Optional</td>
			<td>The product SKU</td>
		</tr>
		<tr>
			<td>weight</td>
			<td>string</td>
			<td>Optional</td>
			<td>The product weight</td>
		</tr>
		<tr>
			<td>stock_number</td>
			<td>string</td>
			<td>Optional</td>
			<td>Total product stock</td>
		</tr>
		<tr>
			<td>title_tag</td>
			<td>string</td>
			<td>Optional</td>
			<td>The product title meta. Used for SEO</td>
		</tr>
		<tr>
			<td>meta_keywords</td>
			<td>string</td>
			<td>Optional</td>
			<td>The product keyword meta. Used for SEO</td>
		</tr>
		<tr>
			<td>meta_description</td>
			<td>string</td>
			<td>Optional</td>
			<td>The product description meta. Used for SEO</td>
		</tr>
		<tr>
			<td>was_price</td>
			<td>INT</td>
			<td>Optional</td>
			<td>The product 'Was Price'</td>
		</tr>
		<tr>
			<td>rrp</td>
			<td>INT</td>
			<td>Optional</td>
			<td>The product recommended retail price (RRP)</td>
		</tr>	
		<tr>
			<td>trade_price</td>
			<td>INT</td>
			<td>Optional</td>
			<td>The product trade price</td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/products/2455436
{% endhighlight %}

{% highlight javascript %}
{ "product" : 
	{
		"ID" : 898440,
		"parent_category" : 123133,
		"title" : "Retro T-Shirt",
		"short_description" : "Quisque sed arcu quis nunc porttitor rutrum faucibus a nunc.",
		"long_description" : "",
		"price" : "25.99",
		"sku" : "898440",
		"weight" : "4.60",
		"stock_number" : 121,
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
			<td>parent_category</td>
			<td>INT</td>
			<td>Optional</td>
			<td>The ID of the category <br /><small>See: <a href="http://createdotnet.github.com/API-Documentation/resources/shop/products_and_categories/categories.html">Categories</a></small></td>
		</tr>
		<tr>
			<td>title</td>
			<td>string</td>
			<td>Required</td>
			<td>The product title</td>
		</tr>
		<tr>
			<td>short_description</td>
			<td>string</td>
			<td>Optional</td>
			<td>The product short description</td>
		</tr>
		<tr>
			<td>long_description</td>
			<td>string</td>
			<td>Optional</td>
			<td>The product long description</td>
		</tr>
		<tr>
			<td>price</td>
			<td>INT</td>
			<td>Required</td>
			<td>The product price</td>
		</tr>
		<tr>
			<td>sku</td>
			<td>string</td>
			<td>Optional</td>
			<td>The product SKU</td>
		</tr>
		<tr>
			<td>weight</td>
			<td>string</td>
			<td>Optional</td>
			<td>The product weight</td>
		</tr>
		<tr>
			<td>stock_number</td>
			<td>string</td>
			<td>Optional</td>
			<td>Total product stock</td>
		</tr>
		<tr>
			<td>title_tag</td>
			<td>string</td>
			<td>Optional</td>
			<td>The product title meta. Used for SEO</td>
		</tr>
		<tr>
			<td>meta_keywords</td>
			<td>string</td>
			<td>Optional</td>
			<td>The product keyword meta. Used for SEO</td>
		</tr>
		<tr>
			<td>meta_description</td>
			<td>string</td>
			<td>Optional</td>
			<td>The product description meta. Used for SEO</td>
		</tr>
		<tr>
			<td>was_price</td>
			<td>INT</td>
			<td>Optional</td>
			<td>The product 'Was Price'</td>
		</tr>
		<tr>
			<td>rrp</td>
			<td>INT</td>
			<td>Optional</td>
			<td>The product recommended retail price (RRP)</td>
		</tr>	
		<tr>
			<td>trade_price</td>
			<td>INT</td>
			<td>Optional</td>
			<td>The product trade price</td>
		</tr>
	</tbody>
</table>
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