Blog Comments
=============

*Access Levels*    
__Group:__ blogs     
__Resource:__ blog_commentss

List all blog Comments
-------------------

```php
GET 	https://api.create.net/blog/comments
```

### Input

```php
GET 	https://api.create.net/blog/comments?post_id=2554
```

@todo Add Inputs

### Response

```console
Status: 200 OK
```

```json
{ "blog_comments":[
	{
		"ADD DATA" : "ADD DATA",
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
		"ADD DATA" : "ADD DATA",
	}
}
```
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