Blog Posts
=============

*Access Levels*    
__Group:__ blogs     
__Resource:__ blog_posts

List all blog posts
-------------------

```php
GET 	https://api.create.net/blog_posts
```

### Input

```php
GET 	https://api.create.net/blog_posts?author=adam
```

* *author* - Name of author [string]
* *datetime_from* - Date and Time of from range [2010-04-07 18:08:14]
* *datetime_to* - Date and Time of to range [2012-06-02 00:00:00]
* *category* - ID of category [int]

### Response

```console
Status: 200 OK
```

```json
{ "blog_posts":[
	{
		"ID" : "3408",
		"category_id" : "2352",
		"title" : "Memorable Walks",
		"post" : "This coastal path goes from Sennen to &lt;a title=&quot;walk to Lands End and Nanjizal Bay - The Times &quot; href=&quot;http://www.timesonline.co.uk/tol/travel/holiday_type/active/article6107981.ece&quot; target=&quot;_blank&quot;&gt;Lands End and then Nanjizal Bay&lt;/a&gt;, or seal cove as we always seem to see seals here. There are some beautiful cliffs, and stunning views out towards the Scily Isles on a clear day. The walk back across the fields has great views of Lands End; a&amp;nbsp;strategically placed cafe is reopening half way back to reward hearty&amp;nbsp;walkers with a cream tea!",
		"author" : "Adam",
		"datetime" : "2011-04-16 14:28:18",
		"title_tag" : "Cliff top walks in West Penwith",
		"meta_keys" : "Cliff top walks Lands End Nanjizal Bay St Just Cap Cornwall Sennen Cove",
		"meta_desc" : "cliff top walks in West Penwith and around Sennen Cove"
	}
]}
```

Get a single blog post
-----------------------

```php
GET 	https://api.create.net/blog_posts/:id
```

### Response

```console
Status: 200 OK
```

```json
{ "blog_post" : 
	{
		"ID" : "3528",
		"category_id" : "2352,1248",
		"title" : "Great Pubs",
		"post" : "The Gurnards Head in Treen is a favourite. Sunday lunch is particularly good but you do need to book. We walked-up Cairn Galver after lunch and the views from Zennor across the peninsular to Penzance are just amazing. We love the fact this stretch of coastline is so wild. ",
		"author" : "Adam",
		"datetime" : "2011-08-06 10:42:12",
		"title_tag" : "Great Pubs in West Penwith",
		"meta_keys" : "Great Pubs Cornwall Sennen Cove",
		"meta_desc" : "Great Pubs in West Penwith and around Sennen Cove"
	}
}
```

Create a blog post
------------------

```php
POST 	https://api.create.net/blog_posts
```

### Input

* *category_id* Optional [int]
* *title* Required [string]
* *post* Required [string]
* *author* Optional [string]
* *datetime* Optional, If not specifed, defaults to datetime of request. [2012-01-14 18:12:18]
* *title_tag* Optional [string]
* *meta_keys* Optional [string]
* *meta_desc* Optional [string]

### Response

```console
Status: 201 Created
Location: http://api.create.net/blog_posts/54648
```

```json
{ "blog_post" : 
	{
		"ID" : "3528",
		"category_id" : "2352,1248",
		"title" : "Great Pubs",
		"post" : "The Gurnards Head in Treen is a favourite. Sunday lunch is particularly good but you do need to book. We walked-up Cairn Galver after lunch and the views from Zennor across the peninsular to Penzance are just amazing. We love the fact this stretch of coastline is so wild. ",
		"author" : "Adam",
		"datetime" : "2011-08-06 10:42:12",
		"title_tag" : "Great Pubs in West Penwith",
		"meta_keys" : "Great Pubs Cornwall Sennen Cove",
		"meta_desc" : "Great Pubs in West Penwith and around Sennen Cove"
	}
}
```

Update a blog post
------------------

```php
PUT 	https://api.create.net/blog_posts/:id
```

### Input

* *category_id* [int]
* *title* [string]
* *post* [string]
* *author* [string]
* *title_tag* [string]
* *meta_keys* [string]
* *meta_desc* [string]

### Response

```console
Status: 200 OK
```

Delete a blog post
------------------

```php
DELETE 	https://api.create.net/blog_posts/:id
```

### Response

```console
Status: 200 OK
```