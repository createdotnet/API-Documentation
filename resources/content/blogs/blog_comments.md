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
			<td>post_id</td>
			<td>INT</td>
			<td>Optional</td>
			<td>Get all blog comments from a single blog post</td>
		</tr>
		<tr>
			<td>datetime_from</td>
			<td>datetime</td>
			<td>Optional</td>
			<td>Comments after a certian date <br /><small>yyyy-mm-dd hh:mm:ss</small></td>
		</tr>
		<tr>
			<td>datetime_to</td>
			<td>datetime</td>
			<td>Optional</td>
			<td>Comments up to a certian date <br /><small>yyyy-mm-dd hh:mm:ss</small></td>
		</tr>
		<tr>
			<td>approved</td>
			<td>INT</td>
			<td>Optional</td>
			<td>Get comments by approved status <br /><small>TRUE = Approved, FALSE = Awaiting Approval</small></td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "blog_comments":[
	{
		"ID" : 464533,
		"post_id" : 3524,
		"name" : "Adam Strawson",
		"email" : "adam@create.net",
		"website" : "http://create.net",
		"message" : "A great article, thanks for helping me solve my problem.",
		"datestamp" : "2012-05-16 15:17:04",
		"approved" : TRUE
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
		"ID" : 464533,
		"post_id" : 3524,
		"name" : "Adam Strawson",
		"email" : "adam@create.net",
		"website" : "http://create.net",
		"message" : "A great article, thanks for helping me solve my problem.",
		"datestamp" : "2012-05-16 15:17:04",
		"approved" : TRUE
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