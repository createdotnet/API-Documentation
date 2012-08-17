---
layout: default
title: Enquires
---

Enquires
=============

*Access Levels*    
__Group:__ content     
__Resource:__ enquires

List all enquires
-------------------

{% highlight php %}
GET 	https://api.create.net/enquirys
{% endhighlight %}

### Input

{% highlight php %}
GET 	https://api.create.net/enquirys?datetime_from=2010-04-07%2018:08:14
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
			<td>datetime_from</td>
			<td>datetime</td>
			<td>Optional</td>
			<td>Enquiries after a certian date <br /><small>yyyy-mm-dd hh:mm:ss</small></td>
		</tr>
		<tr>
			<td>datetime_to</td>
			<td>datetime</td>
			<td>Optional</td>
			<td>Enquiries up to a certian date <br /><small>yyyy-mm-dd hh:mm:ss</small></td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "enquiries" :[
	{
		"ID" : 355766,
		"sender" : "adam@create.net",
		"subject" : "Recent order",
		"message" : "Thanks for the order, I\'m impressed with the quality. Do you also have it in Blue?",
		"datestamp" : "2012-05-16 15:17:04"
	}
]}
{% endhighlight %}

Get a single enquiry
-------------------------

{% highlight php %}
GET 	https://api.create.net/enquirys/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "enquiry" :
	{
		"ID" : 355766,
		"sender" : "adam@create.net",
		"subject" : "Recent order",
		"message" : "Thanks for the order, I\'m impressed with the quality. Do you also have it in Blue?",
		"datestamp" : "2012-05-16 15:17:04"
	}
}
{% endhighlight %}

Delete an enquiry
------------------

{% highlight php %}
DELETE 	https://api.create.net/enquirys/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}