---
layout: default
title: Guestbook
---

Guestbook
=============

*Access Levels*    
__Group:__ content     
__Resource:__ guestbook

List all guestbook entries
--------------------------

{% highlight php %}
GET 	https://api.create.net/guestbook
{% endhighlight %}

### Input

{% highlight php %}
GET 	https://api.create.net/guestbook?datetime_from=2010-04-07%2018:08:14
{% endhighlight %}

* *datetime_from* datetime
* *datetime_to* datetime
* *approved* int

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "guestbook" :[
	{
		"ID" : "1743",
		"name" : "Adam",
		"email" : "adam@create.net",
		"website" : "lmgtfy.com",
		"message" : "Thanks for the advice on the fabric colour, it matched perfectly.",
		"datestamp" : "2008-09-08 19:08:21",
		"approved" : "1"
	}
]}
{% endhighlight %}

Get a single guestbook entry
----------------------------

{% highlight php %}
GET 	https://api.create.net/guestbook/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "guestbook" :
	{
		"ID" : "1743",
		"name" : "Adam",
		"email" : "adam@create.net",
		"website" : "lmgtfy.com",
		"message" : "Thanks for the advice on the fabric colour, it matched perfectly.",
		"datestamp" : "2008-09-08 19:08:21",
		"approved" : "1"
	}
}
{% endhighlight %}

Delete a guestbook entry
------------------------

{% highlight php %}
DELETE 	https://api.create.net/guestbook/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}	