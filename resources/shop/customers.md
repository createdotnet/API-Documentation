---
layout: default
title: Customers
---

Customers
=============

*Access Levels*    
__Group:__ shop     
__Resource:__ customers

Please Note: This relates specifically to Shop Customers and not Website Users. This model includes the additional website user information.

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
	  "ID": 123456,
	  "first_name": "John",
	  "last_name": "Doe",
	  "email": null,
	  "user": {
		"username": "johndoe",
		"created_by": "user",
		"date_created": "2015-02-01 12:30:00",
		"email": "john@doe.com"
	  },
	  "notes": null,
	  "addresses": [
		{
		  "ID": 111222,
		  "first_name": "John",
		  "last_name": "Doe",
		  "address1": "1 New Street",
		  "address2": "",
		  "address3": "",
		  "city": "Brighton",
		  "county": "East Sussex",
		  "country": "GB",
		  "postcode": "BN2 123",
		  "phone": "01234567891",
		  "email": "john@doe.com"
		}
	  ]
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
	  "ID": 123456,
	  "first_name": "John",
	  "last_name": "Doe",
	  "email": null,
	  "user": {
		"username": "johndoe",
		"created_by": "user",
		"date_created": "2015-02-01 12:30:00",
		"email": "john@doe.com"
	  },
	  "notes": null,
	  "addresses": [
		{
		  "ID": 111222,
		  "first_name": "John",
		  "last_name": "Doe",
		  "address1": "1 New Street",
		  "address2": "",
		  "address3": "",
		  "city": "Brighton",
		  "county": "East Sussex",
		  "country": "GB",
		  "postcode": "BN2 123",
		  "phone": "01234567891",
		  "email": "john@doe.com"
		}
	  ]
	}
}
{% endhighlight %}
