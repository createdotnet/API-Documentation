# Blog Posts

*Access Levels*

__Group:__ blogs
__Resource:__ blog_posts

## List all blog posts

```php
GET 	https://api.create.net/blog/posts
```

### Input

@TODO Add Input List

### Response

```console
Status: 200 OK
```

```json
{ "blog_posts":[
	{
		"ADD DATA" : "ADD DATA"
	}
]}
```

## Get a single blog post

```php
GET 	https://api.create.net/blog/posts/:id
```

### Response

```console
Status: 200 OK
```

```json
{ "blog_post":[
	{
		"ADD DATA" : "ADD DATA"
	}
]}
```

## Create a blog post

```php
POST 	https://api.create.net/blog/posts
```

### Input

@TODO Add Input List

### Response

```console
Status: 201 Created
Location: http://api.create.net/blog/posts/54648
```

```json
{ "blog_post":[
	{
		"ADD DATA" : "ADD DATA"
	}
]}
```

## Update a blog post

```php
PUT 	https://api.create.net/blog/posts/:id

### Input

@TODO Add Input List

### Response

```console
Status: 200 OK
```

## Delete a blog post

```php
DELETE 	https://api.create.net/blog/posts/:id
```

### Response

```console
Status: 200 OK
```