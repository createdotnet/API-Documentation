Products
=============

*Access Levels*    
__Group:__ shop, products_and_categories
__Resource:__ products

List all products
-------------------

```php
GET 	https://api.create.net/products
```

### Input

```php
GET 	https://api.create.net/products?category_id=123133
```
* *category_id* [int]

### Response

```console
Status: 200 OK
```

```json
{ "products" :[ 
	{
		"ID" : "898440",
		"parentcat_INC" : "123133",
		"title" : "Retro T-Shirt",
		"shortdesc" : "Quisque sed arcu quis nunc porttitor rutrum faucibus a nunc.",
		"longdesc" : "",
		"price" : "25.99",
		"sku" : "898440",
		"weight" : "4.60",
		"stock_number" : "121",
		"titletag" : "Retro T-Shirt",
		"metakeys" : "Tshirt, retro, clothing",
		"metadesc" : "A retro T-shirt",
		"was_price" : "0.00",
		"rrp" : "0.00",
		"trade_price" : "0.00"
	}
]}
```

Get a product
----------

```php
GET 	https://api.create.net/products/:id
```

### Response

```console
Status: 200 OK
```

```json
{ "products" : 
	{
		"ID" : "898440",
		"parentcat_INC" : "123133",
		"title" : "Retro T-Shirt",
		"shortdesc" : "Quisque sed arcu quis nunc porttitor rutrum faucibus a nunc.",
		"longdesc" : "",
		"price" : "25.99",
		"sku" : "898440",
		"weight" : "4.60",
		"stock_number" : "121",
		"titletag" : "Retro T-Shirt",
		"metakeys" : "Tshirt, retro, clothing",
		"metadesc" : "A retro T-shirt",
		"was_price" : "0.00",
		"rrp" : "0.00",
		"trade_price" : "0.00"
	}
}
```

Create a product
-------------

```php
POST 	https://api.create.net/products
```

### Input

* *parentcat_INC* [int]
* *title* [string]
* *shortdesc* [string]
* *longdesc* [string]
* *price* [int]
* *sku* [int]
* *weight* [int]
* *stock_number* [int]
* *titletag* [string]
* *metakeys* [string]
* *metadesc* [string]
* *was_price* [int]
* *rrp* [int]
* *trade_price* [int]


### Response

```console
Status: 201 Created
Location: http://api.create.net/products/2455436
```

```json
{ "products" : 
	{
		"ID" : "898440",
		"parentcat_INC" : "0",
		"title" : "Retro T-Shirt",
		"shortdesc" : "Quisque sed arcu quis nunc porttitor rutrum faucibus a nunc.",
		"longdesc" : "",
		"price" : "25.99",
		"sku" : "898440",
		"weight" : "4.60",
		"stock_number" : "121",
		"titletag" : "Retro T-Shirt",
		"metakeys" : "Tshirt, retro, clothing",
		"metadesc" : "A retro T-shirt",
		"was_price" : "0.00",
		"rrp" : "0.00",
		"trade_price" : "0.00"
	}
}
```

Update a product
-------------

```php
PUT 	https://api.create.net/products/:id
```

### Input

* *parentcat_INC* [int]
* *title* [string]
* *shortdesc* [string]
* *longdesc* [string]
* *price* [int]
* *sku* [int]
* *weight* [int]
* *stock_number* [int]
* *titletag* [string]
* *metakeys* [string]
* *metadesc* [string]
* *was_price* [int]
* *rrp* [int]
* *trade_price* [int]

### Response

```console
Status: 200 OK
```

Delete a product
-------------

```php
DELETE 	https://api.create.net/products/:id
```

### Response

```console
Status: 200 OK
```