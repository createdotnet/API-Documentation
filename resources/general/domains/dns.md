---
layout: default
title: DNS
---

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

<table>
	<thead>
		<tr>
			<th>Param</th>
			<th>Type</th>
			<th>Required</th>
			<th>Description</th>6
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>domain_id</td>
			<td>INT</td>
			<td>Optional</td>
			<td>The ID of the domain. See <a href="http://createdotnet.github.com/API-Documentation/resources/general/domains/domain_names.html">Domain Names</a></td>
		</tr>
		<tr>
			<td>type</td>
			<td>string</td>
			<td>Optional</td>
			<td>The DNS record type <br /><small>Options: NS, MX, A or CNAME</small></td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "dns" :[ 
	{
		"id" : 242223,
		"domain_id" : 226216,
		"name" : "lifefloat.co.uk",
		"type" : "MX",
		"content" : "mail.create.net",
		"ttl" : 900,
		"prio" : 10,
		"change_date" : NULL
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
		"id" : 242223,
		"domain_id" : 226216,
		"name" : "lifefloat.co.uk",
		"type" : "MX",
		"content" : "mail.create.net",
		"ttl" : 900,
		"prio" : 10,
		"change_date" : NULL
	}
}
{% endhighlight %}

Create a DNS record
------------------

{% highlight php %}
POST 	https://api.create.net/dns
{% endhighlight %}

### Input

<table>
	<thead>
		<tr>
			<th>Param</th>
			<th>Type</th>
			<th>Required</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>domain_id</td>
			<td>INT</td>
			<td>Required</td>
			<td>The ID of the domain. See <a href="http://createdotnet.github.com/API-Documentation/resources/general/domains/domain_names.html">Domain Names</a></td>
		</tr>
		<tr>
			<td>name</td>
			<td>string</td>
			<td>Required</td>
			<td>The record name. <br /><small>IE. www.google.com</small></td>
		</tr>
		<tr>
			<td>type</td>
			<td>string</td>
			<td>Required</td>
			<td>The DNS record type <br /><small>Options: NS, MX, A or CNAME</small></td>
		</tr>
		<tr>
			<td>domain_id</td>
			<td>string</td>
			<td>Required</td>
			<td>The DNS record content. <br /><small>IE. an IP address or domain</small></td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/dns/242823
{% endhighlight %}

{% highlight javascript %}
{ "dns" : 
	{
		"id" : 242823,
		"domain_id" : 226216,
		"name" : "www.lifefloat.co.uk",
		"type" : "CNAME",
		"content" : "lifefloat.co.uk",
		"ttl" : 900,
		"prio" : 0,
		"change_date" : NULL
	}
}
{% endhighlight %}

Update a DNS record
------------------

{% highlight php %}
PUT 	https://api.create.net/dns/:id
{% endhighlight %}

### Input

<table>
	<thead>
		<tr>
			<th>Param</th>
			<th>Type</th>
			<th>Required</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>name</td>
			<td>string</td>
			<td>Optional</td>
			<td>The record name. <br /><small>IE. www.google.com</small></td>
		</tr>
		<tr>
			<td>type</td>
			<td>string</td>
			<td>Optional</td>
			<td>The DNS record type <br /><small>Options: NS, MX, A or CNAME</small></td>
		</tr>
		<tr>
			<td>domain_id</td>
			<td>string</td>
			<td>Optional</td>
			<td>The DNS record content. <br /><small>IE. an IP address or domain</small></td>
		</tr>
	</tbody>
</table>

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