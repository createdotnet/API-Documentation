---
layout: default
title: Customers
---

Customers
=============

*Access Levels*    
__Group:__ shop     
__Resource:__ customers

List all customers
-------------------

{% highlight php %}
GET 	https://api.create.net/customers
{% endhighlight %}


### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{
customers: [
	{
		ID: "123456",
		username: "joe_bloggs",
		email: "joe@bloggs.com",
		active: "1",
		date_created: "2015-01-01 11:12:01"
	}
]}
{% endhighlight %}

Get a single customer
-------------------------

{% highlight php %}
GET 	https://api.create.net/customers/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{
	customer: {
		ID: "123456",
		username: "joe_bloggs",
		email: "joe@bloggs.com",
		active: "1",
		date_created: "2015-01-01 11:12:01"
	}
}
{% endhighlight %}
