---
layout: default
title: Blog Categories
---

Blog Categories
=============

*Access Levels*    
__Group:__ blogs     
__Resource:__ blog_categories

List all blog categories
-------------------

{% highlight php %}
GET 	https://api.create.net/blog_categories
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "blog_categories":[
	{
		"ID" : 26255,
		"name" : "Holidays"
	}
]}
{% endhighlight %}

Get a single blog category
-------------------------

{% highlight php %}
GET 	https://api.create.net/blog_categorys/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "blog_category" : 
	{
		"ID" : 26255,
		"name" : "Holidays"
	}
}
{% endhighlight %}

Create a blog category
------------------

{% highlight php %}
POST 	https://api.create.net/blog_categories
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
			<td>The name of the category</td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/blog_categories/54648
{% endhighlight %}

{% highlight javascript %}
{ "blog_category" : 
	{
		"ID" : 3528,
		"name" : "Cats in hats",
	}
}
{% endhighlight %}

Delete a blog comment
------------------

{% highlight php %}
DELETE 	https://api.create.net/blog_categories/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}