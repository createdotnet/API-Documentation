---
layout: default
title: Account Details
---

Account details
=============

*Access Levels*    
__Group:__ general, site_details     
__Resource:__ account_details

List account details
-------------------

{% highlight php %}
GET 	https://api.create.net/account_details
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight json %}
{ "account_details" :
	{
		"ID" : "73663",
		"userid" : "537",
		"company_name" : "Smiths Sweet Emporium",
		"site_name" : "Smiths Amazing Sweets",
		"address1" : "291 Albert Road",
		"address2" : "",
		"town" : "Brighton",
		"county" : "East Sussex",
		"postcode" : "BN2 4QN",
		"country" : "United Kindom"
		"telephone" : "01273 431234",
		"email" : "adam@smithssweets.net",
		"creation_date" : "2002-06-19 14:18:46",
		"account_type_INC" : "Pro Seller",
		"payment_due_date" : "2014-06-12"
	}
}
{% endhighlight %}

Update account_details
------------------

{% highlight php %}
PUT 	https://api.create.net/account_details
{% endhighlight %}

### Input

* *company_name* string  
* *site_name* string  
* *address1* string
* *address2* string  
* *town* string  
* *county* string  
* *postcode* string  
* *country* string  
* *telephone* string  
* *email* string  

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}