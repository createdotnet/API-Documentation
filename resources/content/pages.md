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
		"page_title" : "Summer Festival",
		"page_type" : "standard",
		"content" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae libero ut odio consequat tempor...",
		"title_tag" : "Summer Festival",
		"meta_keywords" : "summer,festival,fun,wahey",
		"meta_keywords" : "A Summer Festival of fun",
		"isonmenu" : "1",
		"menu_text" : "Summer Festival",
		"page_filename" : "summer-festival",
		"menu_order" : "6",
		"parent_id" : "0"
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
		"page_title" : "Summer Festival",
		"page_type" : "standard",
		"content" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae libero ut odio consequat tempor...",
		"titletag" : "Summer Festival",
		"meta_keywords" : "summer,festival,fun,wahey",
		"metadesc" : "A Summer Festival of fun",
		"isonmenu" : "1",
		"menu_text" : "Summer Festival",
		"page_filename" : "summer-festival",
		"menu_order" : "6",
		"parent_id" : "0"
	}
}
{% endhighlight %}

Create a page
-------------

{% highlight php %}
POST 	https://api.create.net/pages
{% endhighlight %}

### Input

* *page_title* string
* *page_type* standard, dynamic, homepage
* *content* string
* *titletag* string
* *meta_keywords* string
* *metadesc* string
* *isonmenu* boolen
* *menu_text* string
* *page_filename* string
* *menu_order* int
* *parent_id* int

### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/pages/236
{% endhighlight %}

{% highlight javascript %}
{ "page" : 
	{
		"ID" : "2640116",
		"page_title" : "Summer Festival",
		"page_type" : "standard",
		"content" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae libero ut odio consequat tempor...",
		"titletag" : "Summer Festival",
		"meta_keywords" : "summer,festival,fun,wahey",
		"metadesc" : "A Summer Festival of fun",
		"isonmenu" : "1",
		"menu_text" : "Summer Festival",
		"page_filename" : "summer-festival",
		"menu_order" : "6",
		"parent_id" : "0"
	}
}
{% endhighlight %}

Update a page
-------------

{% highlight php %}
PUT 	https://api.create.net/pages/:id
{% endhighlight %}

### Input

* *page_title* string
* *page_type* standard, dynamic, homepage
* *content* string
* *titletag* string
* *meta_keywords* string
* *metadesc* string
* *isonmenu* boolen
* *menu_text* string
* *page_filename* string
* *menu_order* int
* *parent_id* int

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