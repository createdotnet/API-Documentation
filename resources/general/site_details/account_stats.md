---
layout: default
title: Account Stats
---

Account stats
=============

*Access Levels*    
__Group:__ general, site_details     
__Resource:__ account_status

List account stats
-------------------

{% highlight php %}
GET 	https://api.create.net/account_stats
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight json %}
{ "account_stats" :[ 
	{
		"ID" : "236",
		"ADD DATA" : "ADD DATA"
	}
]}
{% endhighlight %}