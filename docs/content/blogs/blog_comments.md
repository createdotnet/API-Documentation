Blog Comments
=============

*Access Levels*    
__Group:__ blogs     
__Resource:__ blog_comments

List all blog comments
-------------------

```php
GET 	https://api.create.net/blog/comments
```

### Input

```php
GET 	https://api.create.net/blog/comments?post_id=2554
```
* *post_id* - ID of a blog post [int] 
* *datetime_from* - Date and Time of from range [2010-04-07 18:08:14]
* *datetime_to* - Date and Time of to range [2012-06-02 00:00:00]

### Response

```console
Status: 200 OK
```

```json
{ "blog_comments":[
	{
		"ID" : "464533",
		"post_id" : "3524",
		"name" : "Adam Strawson",
		"email" : "adam@create.net",
		"website" : "http://create.net",
		"message" : "A great article, thanks for helping me solve my problem.",
		"datestamp" : "2012-05-16 15:17:04",
		"approved" : 1
	}
]}
```

Get a single blog comment
-------------------------

```php
GET 	https://api.create.net/blog/comments/:id
```

### Response

```console
Status: 200 OK
```

```json
{ "blog_comment" :
	{
		"ID" : "464533",
		"post_id" : "3524",
		"name" : "Adam Strawson",
		"email" : "adam@create.net",
		"website" : "http://create.net",
		"message" : "A great article, thanks for helping me solve my problem.",
		"datestamp" : "2012-05-16 15:17:04",
		"approved" : 1
	}
}
```


Delete a blog comment
------------------

```php
DELETE 	https://api.create.net/blog/comments/:id
```

### Response

```console
Status: 200 OK
```