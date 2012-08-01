Categories
=============

*Access Levels*    
__Group:__ shop, products_and_categories
__Resource:__ categories

List all categories
-------------------

```php
GET 	https://api.create.net/categories
```

### Input

```php
GET 	https://api.create.net/categories?parent_category=222608
```
* *parent_category* [int]

### Response

```console
Status: 200 OK
```

```json
{ "categories" :[ 
	{
		"ID" : "271099",
		"parentcat_INC" : "222608",
		"title" : "Hiking",
		"titletag" : "Hiking Gear",
		"metadesc" : "Buy new hiking gear",
		"metakeys" : "hiking, clothing, gear"
	}
]}
```

Get a category
----------

```php
GET 	https://api.create.net/categories/:id
```

### Response

```console
Status: 200 OK
```

```json
{ "categories" : 
	{
		"ID" : "271099",
		"parentcat_INC" : "222608",
		"title" : "Hiking",
		"titletag" : "Hiking Gear",
		"metadesc" : "Buy new hiking gear",
		"metakeys" : "hiking, clothing, gear"
	}
}
```

Create a category
-------------

```php
POST 	https://api.create.net/categories
```

### Input

* *parentcat_INC* [int]
* *title* [string]
* *titletag* [string]
* *metakeys* [string]
* *metadesc* [string]

### Response

```console
Status: 201 Created
Location: http://api.create.net/categories/2455436
```

```json
{ "categories" : 
	{
		"ID" : "271099",
		"parentcat_INC" : "222608",
		"title" : "Hiking",
		"titletag" : "Hiking Gear",
		"metadesc" : "Buy new hiking gear",
		"metakeys" : "hiking, clothing, gear"
	}
}
```

Update a categories
-------------

```php
PUT 	https://api.create.net/categories/:id
```

### Input

* *parentcat_INC* [int]
* *title* [string]
* *titletag* [string]
* *metakeys* [string]
* *metadesc* [string]

### Response

```console
Status: 200 OK
```

Delete a category
-------------

```php
DELETE 	https://api.create.net/categories/:id
```

### Response

```console
Status: 200 OK
```