---
layout: default
title: DNS
---

DNS
=============

*Access Levels*    
__Group:__ general, domains     
__Resource:__ dns

List all DNS records
-------------------

{% highlight php %}
GET 	https://api.create.net/dns
{% endhighlight %}

### Input

{% highlight php %}
GET 	https://api.create.net/dns?domain_id=2672&type=MX
{% endhighlight %}

* *domain_id* int
* *type* NS, MX, A, CNAME

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "dns" :[ 
	{
		"id" : "242223",
		"domain_id" : "226216",
		"name" : "lifefloat.co.uk",
		"type" : "MX",
		"content" : "mail.create.net",
		"ttl" : "900",
		"prio" : "10",
		"change_date" : "NULL"
	}
]}
{% endhighlight %}

Get a single DNS record
-----------------------

{% highlight php %}
GET 	https://api.create.net/dns/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "dns" : 
	{
		"id" : "242223",
		"domain_id" : "226216",
		"name" : "lifefloat.co.uk",
		"type" : "MX",
		"content" : "mail.create.net",
		"ttl" : "900",
		"prio" : "10",
		"change_date" : "NULL"
	}
}
{% endhighlight %}

Create a DNS record
------------------

{% highlight php %}
POST 	https://api.create.net/dns
{% endhighlight %}

### Input

* *domain_id* Required int
* *name* Required string
* *type* Required NS, MX, A, CNAME
* *content* Required string

### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/dns/242823
{% endhighlight %}

{% highlight javascript %}
{ "dns" : 
	{
		"id" : "242823",
		"domain_id" : "226216",
		"name" : "www.lifefloat.co.uk",
		"type" : "CNAME",
		"content" : "lifefloat.co.uk",
		"ttl" : "900",
		"prio" : "0",
		"change_date" : "NULL"
	}
}
{% endhighlight %}

Update a DNS record
------------------

{% highlight php %}
PUT 	https://api.create.net/dns/:id
{% endhighlight %}

### Input

* *name* string
* *type* NS, MX, A, CNAME
* *content* string

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

Delete a DNS record
------------------

{% highlight php %}
DELETE 	https://api.create.net/dns/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}