---
layout: default
title: Categories
---

Categories
=============

*Access Levels*    
__Group:__ shop, products_and_categories  
__Resource:__ categories

List all categories
-------------------

{% highlight php %}
GET 	https://api.create.net/categories
{% endhighlight %}

### Input

{% highlight php %}
GET 	https://api.create.net/categories?parent_category=222608
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
			<td>parent_category</td>
			<td>INT</td>
			<td>Optional</td>
			<td>Get all sub categories with parent ID</td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "categories" :[ 
	{
		"ID" : 271099,
		"parent_category" : 222608,
		"title" : "Hiking",
		"title_tag" : "Hiking Gear",
		"meta_description" : "Buy new hiking gear",
		"meta_keywords" : "hiking, clothing, gear"
	}
]}
{% endhighlight %}

Get a category
----------

{% highlight php %}
GET 	https://api.create.net/categories/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "category" : 
	{
		"ID" : 271099,
		"parent_category" : 222608,
		"title" : "Hiking",
		"title_tag" : "Hiking Gear",
		"meta_description" : "Buy new hiking gear",
		"meta_keywords" : "hiking, clothing, gear"
	}
}
{% endhighlight %}

Create a category
-------------

{% highlight php %}
POST 	https://api.create.net/categories
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
			<td>ID of parent category</td>
		</tr>
		<tr>
			<td>title</td>
			<td>string</td>
			<td>Required</td>
			<td>Title of category</td>
		</tr>
		<tr>
			<td>title_tag</td>
			<td>string</td>
			<td>Optional</td>
			<td>Meta title tag of category. Used for SEO</td>
		</tr>
		<tr>
			<td>meta_keywords</td>
			<td>string</td>
			<td>Optional</td>
			<td>The category keyword meta. Used for SEO</td>
		</tr>
		<tr>
			<td>meta_description</td>
			<td>string</td>
			<td>Optional</td>
			<td>The category description meta. Used for SEO</td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/categories/2455436
{% endhighlight %}

{% highlight javascript %}
{ "category" : 
	{
		"ID" : 271099,
		"parent_category" : 222608,
		"title" : "Hiking",
		"titletag" : "Hiking Gear",
		"meta_description" : "Buy new hiking gear",
		"meta_keywords" : "hiking, clothing, gear"
	}
}
{% endhighlight %}

Update a category
-------------

{% highlight php %}
PUT 	https://api.create.net/categories/:id
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
			<td>ID of parent category</td>
		</tr>
		<tr>
			<td>title</td>
			<td>string</td>
			<td>Optional</td>
			<td>Title of category</td>
		</tr>
		<tr>
			<td>title_tag</td>
			<td>string</td>
			<td>Optional</td>
			<td>Meta title tag of category. Used for SEO</td>
		</tr>
		<tr>
			<td>meta_keywords</td>
			<td>string</td>
			<td>Optional</td>
			<td>The category keyword meta. Used for SEO</td>
		</tr>
		<tr>
			<td>meta_description</td>
			<td>string</td>
			<td>Optional</td>
			<td>The category description meta. Used for SEO</td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

Delete a category
-------------

{% highlight php %}
DELETE 	https://api.create.net/categories/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}