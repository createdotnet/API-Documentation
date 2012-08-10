---
layout: default
title: Domain Names
---

Domain names
=============

*Access Levels*    
__Group:__ general, domains     
__Resource:__ domain_names

List all domain names
-------------------

{% highlight php %}
GET 	https://api.create.net/domain_names
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "domain_names" :[ 
	{
		"ID" : 228025,
		"domain" : "beachfile2.co.uk",
		"date_registered" : "2012-07-17",
		"date_expire" : "2014-07-17",
		"is_primary" : TRUE,
		"is_ourdns" : TRUE
	}
]}
{% endhighlight %}

Get a single domain name
-----------------------

{% highlight php %}
GET 	https://api.create.net/domain_names/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "domain_name" : 
	{
		"ID" : 228025,
		"domain" : "beachfile2.co.uk",
		"date_registered" : "2012-07-17",
		"date_expire" : "2014-07-17",
		"is_primary" : TRUE,
		"is_ourdns" : TRUE
	}
}
{% endhighlight %}

Delete a domain name
------------------

{% highlight php %}
DELETE 	https://api.create.net/domain_names/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}