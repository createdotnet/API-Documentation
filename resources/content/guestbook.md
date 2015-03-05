---
layout: default
title: Guestbook
---

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
			<td>Entries after a certain date <br /><small>yyyy-mm-dd hh:mm:ss</small></td>
		</tr>
		<tr>
			<td>datetime_to</td>
			<td>datetime</td>
			<td>Optional</td>
			<td>Entries up to a certain date <br /><small>yyyy-mm-dd hh:mm:ss</small></td>
		</tr>
		<tr>
			<td>approved</td>
			<td>INT</td>
			<td>Optional</td>
			<td>Get entries by approved status <br /><small>TRUE = Approved, FALSE = Awaiting Approval</small></td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "guestbook" :[
	{
		"ID" : 1743,
		"name" : "Adam",
		"email" : "adam@create.net",
		"website" : "lmgtfy.com",
		"message" : "Thanks for the advice on the fabric colour, it matched perfectly.",
		"datetime" : "2008-09-08 19:08:21",
		"approved" : TRUE
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
		"ID" : 1743,
		"name" : "Adam",
		"email" : "adam@create.net",
		"website" : "lmgtfy.com",
		"message" : "Thanks for the advice on the fabric colour, it matched perfectly.",
		"datetime" : "2008-09-08 19:08:21",
		"approved" : TRUE
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