Blog Categories
=============

*Access Levels*    
__Group:__ blogs     
__Resource:__ blog_categories

List all blog categories
-------------------

```php
GET 	https://api.create.net/blog/categories
```

### Input

```php
GET 	https://api.create.net/blog/categories
```

### Response

```console
Status: 200 OK
```

```json
{ "blog_categories":[
	{
		"ID" : "26255",
		"name" : "Holidays"
	}
]}
```

Get a single blog category
-------------------------

```php
GET 	https://api.create.net/blog/categorys/:id
```

### Response

```console
Status: 200 OK
```

```json
{ "blog_category" : 
	{
		"ID" : "26255",
		"name" : "Holidays"
	}
}
```

Create a blog category
------------------

```php
POST 	https://api.create.net/blog/categories
```

### Input

* *name* Requried [string]

### Response

```console
Status: 201 Created
Location: http://api.create.net/blog/categories/54648
```

```json
{ "blog_post" : 
	{
		"ID" : "3528",
		"name" : "Cats in hats",
	}
}
```

Delete a blog comment
------------------

```php
DELETE 	https://api.create.net/blog/categories/:id
```

### Response

```console
Status: 200 OK
```