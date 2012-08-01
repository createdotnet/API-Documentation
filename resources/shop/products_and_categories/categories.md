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

* *parent_category* int

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "categories" :[ 
	{
		"ID" : "271099",
		"parentcat_INC" : "222608",
		"title" : "Hiking",
		"titletag" : "Hiking Gear",
		"metadesc" : "Buy new hiking gear",
		"metakeys" : "hiking, clothing, gear"
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
{ "categories" : 
	{
		"ID" : "271099",
		"parentcat_INC" : "222608",
		"title" : "Hiking",
		"titletag" : "Hiking Gear",
		"metadesc" : "Buy new hiking gear",
		"metakeys" : "hiking, clothing, gear"
	}
}
{% endhighlight %}

Create a category
-------------

{% highlight php %}
POST 	https://api.create.net/categories
{% endhighlight %}

### Input

* *parentcat_INC* int
* *title* string
* *titletag* string
* *metakeys* string
* *metadesc* string

### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/categories/2455436
{% endhighlight %}

{% highlight javascript %}
{ "categories" : 
	{
		"ID" : "271099",
		"parentcat_INC" : "222608",
		"title" : "Hiking",
		"titletag" : "Hiking Gear",
		"metadesc" : "Buy new hiking gear",
		"metakeys" : "hiking, clothing, gear"
	}
}
{% endhighlight %}

Update a categories
-------------

{% highlight php %}
PUT 	https://api.create.net/categories/:id
{% endhighlight %}

### Input

* *parentcat_INC* int
* *title* string
* *titletag* string
* *metakeys* string
* *metadesc* string

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