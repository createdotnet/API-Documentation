---
layout: default
title: Delivery Zones
---

Delivery Zones
=============

*Access Levels*    
__Group:__ shop     
__Resource:__ deliveryzones

List all delivery types for a zone
-------------------

{% highlight php %}
GET 	https://api.create.net/deliveryzones/:id/types
{% endhighlight %}


### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}

	{
		"delivery_types": [
			{
				"ID": 54321,
				"name": "Royal mail"
			},
			{
				"ID": 54322,
				"name": "Express delivery"
			},
			{
				"ID": 54323,
				"name": "Local pickup"
			}
		]
	}

{% endhighlight %}

Get a single delivery zone
-------------------------

{% highlight php %}
GET 	https://api.create.net/deliveryzones/:id/types/:typeid
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}

{
	delivery_type: {
		"ID": 54321,
		"name": "Royal mail"
	}
}

{% endhighlight %}
