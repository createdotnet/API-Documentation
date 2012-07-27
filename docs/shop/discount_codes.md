Discount Codes
=============

*Access Levels*    
__Group:__ shop
__Resource:__ discount_codes

List all discount codes
-----------------------

```php
GET 	https://api.create.net/discount_codes
```

### Response

```console
Status: 200 OK
```

```json
{ "discount_codes" :[ 
	{
		"ID" : "5890",
		"name" : "Facebook Friends Discount",
		"code" : "FBF010",
		"type" : "percent",
		"amount" : "10.00",
		"expiry" : "0000-00-00"
	}
]}
```

Get a discount code
-------------------

```php
GET 	https://api.create.net/discount_codes/:id
```

### Response

```console
Status: 200 OK
```

```json
{ "discount_codes" : 
	{
		"ID" : "5890",
		"name" : "Facebook Friends Discount",
		"code" : "FBF010",
		"type" : "percent",
		"amount" : "10.00",
		"expiry" : "0000-00-00"
	}
}
```

Create a discount code
----------------------

```php
POST 	https://api.create.net/discount_codes
```

### Input

* *name* [string]
* *code* [string]
* *type* ['percent', 'amount']
* *amount* [int]
* *expiry* [0000-00-00]

### Response

```console
Status: 201 Created
Location: http://api.create.net/discount_codes/236
```

```json
{ "discount_codes" : 
	{
		"ID" : "5890",
		"name" : "Facebook Friends Discount",
		"code" : "FBF010",
		"type" : "percent",
		"amount" : "10.00",
		"expiry" : "0000-00-00"
	}
}
```

Update a discount code
----------------------

```php
PUT 	https://api.create.net/discount_codes/:id
```

### Input

* *name* [string]
* *code* [string]
* *type* ['percent', 'amount']
* *amount* [int]
* *expiry* [0000-00-00]

### Response

```console
Status: 200 OK
```

Delete a discount code
----------------------

```php
DELETE 	https://api.create.net/discount_codes/:id
```

### Response

```console
Status: 200 OK
```