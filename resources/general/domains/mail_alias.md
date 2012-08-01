---
layout: default
title: Email Forwarding
---

Domain mail alias
=============

*Access Levels*    
__Group:__ general, domains     
__Resource:__ mail_alias

List all mail alias
-------------------

{% highlight php %}
GET 	https://api.create.net/mail_alias
{% endhighlight %}

### Input

{% highlight php %}
GET 	https://api.create.net/mail_alias?domain_id=2672
{% endhighlight %}

* *domain_id* - ID of domain int

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "mail_alias" :[ 
	{
		"ID" : "236",
		"domain_id" : "2672",
		"alias" : "help",
		"email" : "adam@create.net"
	}
]}
{% endhighlight %}

Get a single mail alias
-----------------------

{% highlight php %}
GET 	https://api.create.net/mail_alias/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "mail_alias" : 
	{
		"ID" : "236",
		"domain_id" : "2672",
		"alias" : "help",
		"email" : "adam@create.net"
	}
}
{% endhighlight %}

Create a mail alias
------------------

{% highlight php %}
POST 	https://api.create.net/mail_alias
{% endhighlight %}

### Input

* *domain_id* Required int
* *alias* Required string
* *email* Required string

### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/mail_alias/236
{% endhighlight %}

{% highlight javascript %}
{ "mail_alias" : 
	{
		"ID" : "236",
		"domain_id" : "2672",
		"alias" : "help",
		"email" : "adam@create.net"
	}
}
{% endhighlight %}

Update a mail alias
------------------

{% highlight php %}
PUT 	https://api.create.net/mail_alias/:id
{% endhighlight %}

### Input

* *alias* string
* *email* Forwarding address string

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

Delete a mail alias
------------------

{% highlight php %}
DELETE 	https://api.create.net/mail_alias/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}