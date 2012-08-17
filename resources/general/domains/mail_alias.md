---
layout: default
title: Mail Forwarding
---

Mail Forwarding
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
			<td>Optional</td>
			<td>The ID of the domain. See <a href="http://createdotnet.github.com/API-Documentation/resources/general/domains/domain_names.html">Domain Names</a></td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "mail_alias" :[ 
	{
		"ID" : 236,
		"domain_id" : 2672,
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
		"ID" : 236,
		"domain_id" : 2672,
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
			<td>alias</td>
			<td>string</td>
			<td>Required</td>
			<td>The alias of the forwarding address <br /><small>Example: info (Will become: info@mydomain.com)</small></td>
		</tr>
		<tr>
			<td>email</td>
			<td>string</td>
			<td>Required</td>
			<td>The email address to forward to. <br /><small>Example: adam@create.net</small></td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/mail_alias/236
{% endhighlight %}

{% highlight javascript %}
{ "mail_alias" : 
	{
		"ID" : 236,
		"domain_id" : 2672,
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
			<td>alias</td>
			<td>string</td>
			<td>Optional</td>
			<td>The alias of the forwarding address <br /><small>Example: info (Will become: info@mydomain.com)</small></td>
		</tr>
		<tr>
			<td>email</td>
			<td>string</td>
			<td>Optional</td>
			<td>The email address to forward to. <br /><small>Example: adam@create.net</small></td>
		</tr>
	</tbody>
</table>

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