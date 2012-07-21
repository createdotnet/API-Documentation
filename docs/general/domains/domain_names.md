Domain names
=============

*Access Levels*    
__Group:__ general, domains     
__Resource:__ domain_names

List all domain names
-------------------

```php
GET 	https://api.create.net/domain/domain_names
```

### Input

@TODO

### Response

```console
Status: 200 OK
```

```json
{ "domain_names" :[ 
	{
		"ID" : "236",
		"ADD DATA" : "ADD DATA"
	}
]}
```

Get a single domain name
-----------------------

```php
GET 	https://api.create.net/domain/domain_names/:id
```

### Response

```console
Status: 200 OK
```

```json
{ "domain_name" : 
	{
		"ID" : "236",
		"ADD DATA" : "ADD DATA"
	}
}
```

Create a domain name
------------------

@TODO - Speak to Joel, is this possible?

Update a domain name
------------------

```php
PUT 	https://api.create.net/domain/domain_names/:id
```

### Input

@TODO

### Response

```console
Status: 200 OK
```

Delete a domain name
------------------

```php
DELETE 	https://api.create.net/domain/domain_names/:id
```

### Response

```console
Status: 200 OK
```