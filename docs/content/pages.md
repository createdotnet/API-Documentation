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

### Response

```console
Status: 200 OK
```

```json
{ "pages" :[ 
	{
		"ID" : "2640116",
		"pagetitle" : "Summer Festival",
		"pagetype" : "standard",
		"content" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae libero ut odio consequat tempor...",
		"titletag" : "Summer Festival",
		"metakeys" : "summer,festival,fun,wahey",
		"metadesc" : "A Summer Festival of fun",
		"onmenu_YN" : "1",
		"menutext" : "Summer Festival",
		"pagefilename" : "summer-festival",
		"menuorder" : "6",
		"parentid" : "0"
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
		"ID" : "2640116",
		"pagetitle" : "Summer Festival",
		"pagetype" : "standard",
		"content" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae libero ut odio consequat tempor...",
		"titletag" : "Summer Festival",
		"metakeys" : "summer,festival,fun,wahey",
		"metadesc" : "A Summer Festival of fun",
		"onmenu_YN" : "1",
		"menutext" : "Summer Festival",
		"pagefilename" : "summer-festival",
		"menuorder" : "6",
		"parentid" : "0"
	}
}
```

Create a page
-------------

```php
POST 	https://api.create.net/pages
```

### Input

* *pagetitle* [string]
* *pagetype* ['standard', 'dynamic', 'homepage']
* *content* [string]
* *titletag* [string]
* *metakeys* [string]
* *metadesc* [string]
* *onmenu_YN* [boolen]
* *menutext* [string]
* *pagefilename* [string]
* *menuorder* [int]
* *parentid* [int]

### Response

```console
Status: 201 Created
Location: http://api.create.net/pages/236
```

```json
{ "pages" : 
	{
		"ID" : "2640116",
		"pagetitle" : "Summer Festival",
		"pagetype" : "standard",
		"content" : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae libero ut odio consequat tempor...",
		"titletag" : "Summer Festival",
		"metakeys" : "summer,festival,fun,wahey",
		"metadesc" : "A Summer Festival of fun",
		"onmenu_YN" : "1",
		"menutext" : "Summer Festival",
		"pagefilename" : "summer-festival",
		"menuorder" : "6",
		"parentid" : "0"
	}
}
```

Update a page
-------------

```php
PUT 	https://api.create.net/pages/:id
```

### Input

* *pagetitle* [string]
* *pagetype* ['standard', 'dynamic', 'homepage']
* *content* [string]
* *titletag* [string]
* *metakeys* [string]
* *metadesc* [string]
* *onmenu_YN* [boolen]
* *menutext* [string]
* *pagefilename* [string]
* *menuorder* [int]
* *parentid* [int]

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