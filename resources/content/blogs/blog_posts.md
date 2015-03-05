---
layout: default
title: Blog Posts
---

*Access Levels*    
__Group:__ blogs     
__Resource:__ blogs

List all blog posts
-------------------

{% highlight php %}
GET 	https://api.create.net/blogs
{% endhighlight %}

### Input

{% highlight php %}
GET 	https://api.create.net/blogs?author=adam
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
			<td>author</td>
			<td>string</td>
			<td>Optional</td>
			<td>The name of the author.</td>
		</tr>
		<tr>
			<td>datetime_from</td>
			<td>datetime</td>
			<td>Optional</td>
			<td>Posts after a certain date <br /><small>yyyy-mm-dd hh:mm:ss</small></td>
		</tr>
		<tr>
			<td>datetime_to</td>
			<td>datetime</td>
			<td>Optional</td>
			<td>Posts up to a certain date <br /><small>yyyy-mm-dd hh:mm:ss</small></td>
		</tr>
		<tr>
			<td>category</td>
			<td>array</td>
			<td>Optional</td>
			<td>Array of category IDs</td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "blogs":[
	{
		"ID" : 3408,
		"category_id" : [2352],
		"title" : "Memorable Walks",
		"post" : "This coastal path goes from Sennen to &lt;a title=&quot;walk to Lands End and Nanjizal Bay - The Times &quot; href=&quot;http://www.timesonline.co.uk/tol/travel/holiday_type/active/article6107981.ece&quot; target=&quot;_blank&quot;&gt;Lands End and then Nanjizal Bay&lt;/a&gt;, or seal cove as we always seem to see seals here. There are some beautiful cliffs, and stunning views out towards the Scily Isles on a clear day. The walk back across the fields has great views of Lands End; a&amp;nbsp;strategically placed cafe is reopening half way back to reward hearty&amp;nbsp;walkers with a cream tea!",
		"author" : "Adam",
		"datetime" : "2011-04-16 14:28:18",
		"title_tag" : "Cliff top walks in West Penwith",
		"meta_keywords" : "Cliff top walks Lands End Nanjizal Bay St Just Cap Cornwall Sennen Cove",
		"meta_description" : "cliff top walks in West Penwith and around Sennen Cove"
	}
]}
{% endhighlight %}

Get a single blog post
-----------------------

{% highlight php %}
GET 	https://api.create.net/blogs/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "blog_post" : 
	{
		"ID" : 3528,
		"category_id" : [2352, 1248],
		"title" : "Great Pubs",
		"post" : "The Gurnards Head in Treen is a favorite. Sunday lunch is particularly good but you do need to book. We walked-up Cairn Galver after lunch and the views from Zennor across the peninsular to Penzance are just amazing. We love the fact this stretch of coastline is so wild. ",
		"author" : "Adam",
		"datetime" : "2011-08-06 10:42:12",
		"title_tag" : "Great Pubs in West Penwith",
		"meta_keywords" : "Great Pubs Cornwall Sennen Cove",
		"meta_description" : "Great Pubs in West Penwith and around Sennen Cove"
	}
}
{% endhighlight %}

Create a blog post
------------------

{% highlight php %}
POST 	https://api.create.net/blogs
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
			<td>category_id</td>
			<td>array</td>
			<td>Optional</td>
			<td>Array of category IDs</td>
		</tr>
		<tr>
			<td>title</td>
			<td>string</td>
			<td>Required</td>
			<td>Title of the blog post</td>
		</tr>
		<tr>
			<td>post</td>
			<td>string</td>
			<td>Required</td>
			<td>Content of the blog post <br /><small>Plain text and HTML accepted</small></td>
		</tr>
		<tr>
			<td>author</td>
			<td>string</td>
			<td>Optional</td>
			<td>The name of the author.</td>
		</tr>
		<tr>
			<td>title_tag</td>
			<td>string</td>
			<td>Optional</td>
			<td>Title meta tag of the blog post. Used for SEO</td>
		</tr>
		<tr>
			<td>meta_keywords</td>
			<td>string</td>
			<td>Optional</td>
			<td>Keywords meta of the blog post. Used for SEO</td>
		</tr>
		<tr>
			<td>meta_description</td>
			<td>string</td>
			<td>Optional</td>
			<td>Description meta tag of the blog post. Used for SEO</td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 201 Created
{% endhighlight %}

{% highlight javascript %}
{
    "ID": 101775,
    "_links": {
        "self": "/blogs/101775"
    }
}
{% endhighlight %}

Update a blog post
------------------

{% highlight php %}
PUT 	https://api.create.net/blogs/:id
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
			<td>category_id</td>
			<td>array</td>
			<td>Optional</td>
			<td>Array of category IDs</td>
		</tr>
		<tr>
			<td>title</td>
			<td>string</td>
			<td>Optional</td>
			<td>Title of the blog post</td>
		</tr>
		<tr>
			<td>post</td>
			<td>string</td>
			<td>Optional</td>
			<td>Content of the blog post <br /><small>Plain text and HTML accepted</small></td>
		</tr>
		<tr>
			<td>author</td>
			<td>string</td>
			<td>Optional</td>
			<td>The name of the author.</td>
		</tr>
		<tr>
			<td>title_tag</td>
			<td>string</td>
			<td>Optional</td>
			<td>Title meta tag of the blog post. <br /><small>Used for SEO</small></td>
		</tr>
		<tr>
			<td>meta_keywords</td>
			<td>string</td>
			<td>Optional</td>
			<td>Keywords meta of the blog post. <br /><small>Used for SEO</small></td>
		</tr>
		<tr>
			<td>meta_description</td>
			<td>string</td>
			<td>Optional</td>
			<td>Description meta tag of the blog post. <br /><small>Used for SEO</small></td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

Delete a blog post
------------------

{% highlight php %}
DELETE 	https://api.create.net/blogs/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}
