---
layout: default
title: Delivery Zones
---

Delivery Zones
=============

*Access Levels*    
__Group:__ shop     
__Resource:__ deliveryzones

List all delivery zones
-------------------

{% highlight php %}
GET 	https://api.create.net/deliveryzones
{% endhighlight %}


### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}

	{
		"delivery_zones" : [
			{
				"ID"                          : 12345,
				"name"                        : "Home Country",
				"tax_enabled"                 : true,
				"prices_are_exclusive_of_tax" : true,
				"charge_tax_in_this_zone"     : true,
				"tax_name"                    : "VAT",
				"tax_rate"                    : 20,
				"free_postage_above"          : "0.00"
			},
			{
				"ID"                          : 12346,
				"name"                        : "America",
				"tax_enabled"                 : false,
				"prices_are_exclusive_of_tax" : false,
				"charge_tax_in_this_zone"     : false,
				"tax_name"                    : "",
				"tax_rate"                    : "0.00",
				"free_postage_above"          : "0.00"
			},
			{
				"ID"                          : 12347,
				"name"                        : "Europe",
				"tax_enabled"                 : false,
				"prices_are_exclusive_of_tax" : false,
				"charge_tax_in_this_zone"     : false,
				"tax_name"                    : "",
				"tax_rate"                    : "0.00",
				"free_postage_above"          : "0.00"
			},
			{
				"ID"                          : 12348,
				"name"                        : "All Other Countries",
				"tax_enabled"                 : false,
				"prices_are_exclusive_of_tax" : false,
				"charge_tax_in_this_zone"     : false,
				"tax_name"                    : "",
				"tax_rate"                    : "0.00",
				"free_postage_above"          : "0.00"
			}
		]
	}

{% endhighlight %}

Get a single delivery zone
-------------------------

{% highlight php %}
GET 	https://api.create.net/deliveryzones/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}

{
	delivery_zone: {
		"ID"                          : 12348,
		"name"                        : "All Other Countries",
		"tax_enabled"                 : false,
		"prices_are_exclusive_of_tax" : false,
		"charge_tax_in_this_zone"     : false,
		"tax_name"                    : "",
		"tax_rate"                    : "0.00",
		"free_postage_above"          : "0.00"
	}
}

{% endhighlight %}
