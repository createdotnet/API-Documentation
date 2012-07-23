Pages
=============

*Access Levels*    
__Group:__ content
__Resource:__ pages

List all pages
-------------------

```php
GET 	https://api.create.net/pages
```

### Input

@TODO

### Response

```console
Status: 200 OK
```

```json
{ "pages" :[ 
	{
		"ID" : "236",
		"ADD DATA" : "ADD DATA"
	}
]}
```

Get a page
----------

```php
GET 	https://api.create.net/pages/:id
```

### Response

```console
Status: 200 OK
```

```json
{ "pages" : 
	{
		"ID" : "236",
		"ADD DATA" : "ADD DATA"
	}
}
```

Create a page
-------------

```php
POST 	https://api.create.net/pages
```

### Input

@TODO

### Response

```console
Status: 201 Created
Location: http://api.create.net/pages/236
```

```json
{ "pages" : 
	{
		"ID" : "236",
		"ADD DATA" : "ADD DATA"
	}
}
```

Update a page
-------------

```php
PUT 	https://api.create.net/pages/:id
```

### Input

@TODO

### Response

```console
Status: 200 OK
```

Delete a page
-------------

```php
DELETE 	https://api.create.net/pages/:id
```

### Response

```console
Status: 200 OK
```