---
layout: default
title: Pages
---

Pages
=============

*Access Levels*    
__Group:__ content
__Resource:__ pages

List all pages
-------------------

{% highlight php %}
GET 	https://api.create.net/pages
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "pages" :[ 
	{
		"ID" : "2640116",
		"pagetitle" : "Summer Festival",
		"pagetype" : "standard",
		"content" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae libero ut odio consequat tempor...",
		"titletag" : "Summer Festival",
		"metakeys" : "summer,festival,fun,wahey",
		"metadesc" : "A Summer Festival of fun",
		"onmenu_YN" : "1",
		"menutext" : "Summer Festival",
		"pagefilename" : "summer-festival",
		"menuorder" : "6",
		"parentid" : "0"
	}
]}
{% endhighlight %}

Get a page
----------

{% highlight php %}
GET 	https://api.create.net/pages/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "page" : 
	{
		"ID" : "2640116",
		"pagetitle" : "Summer Festival",
		"pagetype" : "standard",
		"content" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae libero ut odio consequat tempor...",
		"titletag" : "Summer Festival",
		"metakeys" : "summer,festival,fun,wahey",
		"metadesc" : "A Summer Festival of fun",
		"onmenu_YN" : "1",
		"menutext" : "Summer Festival",
		"pagefilename" : "summer-festival",
		"menuorder" : "6",
		"parentid" : "0"
	}
}
{% endhighlight %}

Create a page
-------------

{% highlight php %}
POST 	https://api.create.net/pages
{% endhighlight %}

### Input

* *pagetitle* string
* *pagetype* standard, dynamic, homepage
* *content* string
* *titletag* string
* *metakeys* string
* *metadesc* string
* *onmenu_YN* boolen
* *menutext* string
* *pagefilename* string
* *menuorder* int
* *parentid* int

### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/pages/236
{% endhighlight %}

{% highlight javascript %}
{ "page" : 
	{
		"ID" : "2640116",
		"pagetitle" : "Summer Festival",
		"pagetype" : "standard",
		"content" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae libero ut odio consequat tempor...",
		"titletag" : "Summer Festival",
		"metakeys" : "summer,festival,fun,wahey",
		"metadesc" : "A Summer Festival of fun",
		"onmenu_YN" : "1",
		"menutext" : "Summer Festival",
		"pagefilename" : "summer-festival",
		"menuorder" : "6",
		"parentid" : "0"
	}
}
{% endhighlight %}

Update a page
-------------

{% highlight php %}
PUT 	https://api.create.net/pages/:id
{% endhighlight %}

### Input

* *pagetitle* string
* *pagetype* standard, dynamic, homepage
* *content* string
* *titletag* string
* *metakeys* string
* *metadesc* string
* *onmenu_YN* boolen
* *menutext* string
* *pagefilename* string
* *menuorder* int
* *parentid* int

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

Delete a page
-------------

{% highlight php %}
DELETE 	https://api.create.net/pages/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}