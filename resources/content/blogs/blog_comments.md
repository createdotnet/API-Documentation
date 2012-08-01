---
layout: default
title: Blog Comments
---

Blog Comments
=============

*Access Levels*    
__Group:__ blogs     
__Resource:__ blog_comments

List all blog comments
-------------------

{% highlight php %}
GET 	https://api.create.net/blog_comments
{% endhighlight %}

### Input

{% highlight php %}
GET 	https://api.create.net/blog_comments?post_id=2554
{% endhighlight %}

* *post_id* int
* *datetime_from* datetime
* *datetime_to* datetime

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "blog_comments":[
	{
		"ID" : "464533",
		"post_id" : "3524",
		"name" : "Adam Strawson",
		"email" : "adam@create.net",
		"website" : "http://create.net",
		"message" : "A great article, thanks for helping me solve my problem.",
		"datestamp" : "2012-05-16 15:17:04",
		"approved" : "1"
	}
]}
{% endhighlight %}

Get a single blog comment
-------------------------

{% highlight php %}
GET 	https://api.create.net/blog_comments/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "blog_comment" :
	{
		"ID" : "464533",
		"post_id" : "3524",
		"name" : "Adam Strawson",
		"email" : "adam@create.net",
		"website" : "http://create.net",
		"message" : "A great article, thanks for helping me solve my problem.",
		"datestamp" : "2012-05-16 15:17:04",
		"approved" : "1"
	}
}
{% endhighlight %}


Delete a blog comment
------------------

{% highlight php %}
DELETE 	https://api.create.net/blog_comments/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}