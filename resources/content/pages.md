---
layout: default
title: Pages
---

Pages
=============

*Access Levels*    
__Group:__ content   
__Resource:__ pages

List all pages
-------------------

{% highlight php %}
GET 	https://api.create.net/pages
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "pages" :[ 
	{
		"ID" : 2640116,
		"page_title" : "Summer Festival",
		"page_type" : "standard",
		"content" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae libero ut odio consequat tempor...",
		"title_tag" : "Summer Festival",
		"meta_keywords" : "summer,festival,fun,wahey",
		"meta_description" : "A Summer Festival of fun",
		"is_onmenu" : TRUE,
		"menu_text" : "Summer Festival",
		"page_filename" : "summer-festival",
		"menu_order" : 6,
		"parent_id" : 0,
		"data_set" : NULL
	},
	{
		"ID" : 2640248,
		"page_title" : "Festival Blog",
		"page_type" : "dynamic",
		"content" : NULL,
		"title_tag" : "Our Festival Blog",
		"meta_keywords" : "blog,festival,fun,wahey",
		"meta_description" : "A blog about our Festivals",
		"is_onmenu" : TRUE,
		"menu_text" : "Blog",
		"page_filename" : "festival-blog",
		"menu_order" : 7,
		"parent_id" : 0,
		"data_set" : "https://api.create.net/blog_posts"
	}
]}
{% endhighlight %}

### Dynamic Pages

If the page is a dynamic page, the content will be NULL, an additional request will be required to retreive content speciic to the page. The relevant method is specified in "data_set".

The following pages are dynamic:
* News
* Events
* Links
* External Links
* Contact
* Tell a friend
* Shop
* Blog
* Guestbook

Get a page
----------

{% highlight php %}
GET 	https://api.create.net/pages/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "page" : 
	{
		"ID" : 2640116,
		"page_title" : "Summer Festival",
		"page_type" : "standard",
		"content" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae libero ut odio consequat tempor...",
		"title_tag" : "Summer Festival",
		"meta_keywords" : "summer,festival,fun,wahey",
		"meta_description" : "A Summer Festival of fun",
		"is_onmenu" : TRUE,
		"menu_text" : "Summer Festival",
		"page_filename" : "summer-festival",
		"menu_order" : 6,
		"parent_id" : 0
	}
}
{% endhighlight %}

Create a page
-------------

{% highlight php %}
POST 	https://api.create.net/pages
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
			<td>page_title</td>
			<td>string</td>
			<td>Required</td>
			<td>The page title</td>
		</tr>
		<tr>
			<td>page_type</td>
			<td>string</td>
			<td>Required</td>
			<td>The page type <br /><small>Options: standard, dynamic, or homepage</small></td>
		</tr>
		<tr>
			<td>content</td>
			<td>string</td>
			<td>Required</td>
			<td>The page content <br /><small>Options: If page_type is standard or homepage then Text or HTML, if page_type is dynamic then, news, events, links, external, contact, shop, blog or guestbook</small></td>
		</tr>
		<tr>
			<td>title_tag</td>
			<td>string</td>
			<td>Optional</td>
			<td>Title meta tag of the page. Used for SEO</td>
		</tr>
		<tr>
			<td>meta_keywords</td>
			<td>string</td>
			<td>Optional</td>
			<td>Keywords meta of the page. Used for SEO</td>
		</tr>
		<tr>
			<td>meta_description</td>
			<td>string</td>
			<td>Optional</td>
			<td>Description meta tag of the page. Used for SEO</td>
		</tr>
		<tr>
			<td>is_onmenu</td>
			<td>Boolean</td>
			<td>Required</td>
			<td>Show this page on your menu. <br /><small>TRUE = Yes, False = No</small></td>
		</tr>
		<tr>
			<td>menu_text</td>
			<td>string</td>
			<td>Required</td>
			<td>The text for the menu item</td>
		</tr>
		<tr>
			<td>page_filename</td>
			<td>string</td>
			<td>Required</td>
			<td>The filename of the page</td>
		</tr>
		<tr>
			<td>menu_order</td>
			<td>INT</td>
			<td>Required</td>
			<td>The menu position of the page</td>
		</tr>
		<tr>
			<td>parent_id</td>
			<td>INT</td>
			<td>Optional</td>
			<td>Used for creating parent and sub-pages.</td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 201 Created
Location: http://api.create.net/pages/236
{% endhighlight %}

{% highlight javascript %}
{ "page" : 
	{
		"ID" : 2640116,
		"page_title" : "Summer Festival",
		"page_type" : "standard",
		"content" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae libero ut odio consequat tempor...",
		"title_tag" : "Summer Festival",
		"meta_keywords" : "summer,festival,fun,wahey",
		"meta_description" : "A Summer Festival of fun",
		"is_onmenu" : TRUE,
		"menu_text" : "Summer Festival",
		"page_filename" : "summer-festival",
		"menu_order" : 6,
		"parent_id" : 0
	}
}
{% endhighlight %}

Update a page
-------------

{% highlight php %}
PUT 	https://api.create.net/pages/:id
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
			<td>page_title</td>
			<td>string</td>
			<td>Optional</td>
			<td>The page title</td>
		</tr>
		<tr>
			<td>page_type</td>
			<td>string</td>
			<td>Optional</td>
			<td>The page type <br /><small>Options: standard, dynamic, or homepage</small></td>
		</tr>
		<tr>
			<td>content</td>
			<td>string</td>
			<td>Optional</td>
			<td>The page content <br /><small>Options: If page_type is standard or homepage then Text or HTML, if page_type is dynamic then, news, events, links, external, contact, shop, blog or guestbook</small></td>
		</tr>
		<tr>
			<td>title_tag</td>
			<td>string</td>
			<td>Optional</td>
			<td>Title meta tag of the page. Used for SEO</td>
		</tr>
		<tr>
			<td>meta_keywords</td>
			<td>string</td>
			<td>Optional</td>
			<td>Keywords meta of the page. Used for SEO</td>
		</tr>
		<tr>
			<td>meta_description</td>
			<td>string</td>
			<td>Optional</td>
			<td>Description meta tag of the page. Used for SEO</td>
		</tr>
		<tr>
			<td>is_onmenu</td>
			<td>Boolean</td>
			<td>Optional</td>
			<td>Show this page on your menu. <br /><small>TRUE = Yes, False = No</small></td>
		</tr>
		<tr>
			<td>menu_text</td>
			<td>string</td>
			<td>Optional</td>
			<td>The text for the menu item</td>
		</tr>
		<tr>
			<td>page_filename</td>
			<td>string</td>
			<td>Optional</td>
			<td>The filename of the page</td>
		</tr>
		<tr>
			<td>menu_order</td>
			<td>INT</td>
			<td>Optional</td>
			<td>The menu position of the page</td>
		</tr>
		<tr>
			<td>parent_id</td>
			<td>INT</td>
			<td>Optional</td>
			<td>Used for creating parent and sub-pages.</td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

Delete a page
-------------

{% highlight php %}
DELETE 	https://api.create.net/pages/:id
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}