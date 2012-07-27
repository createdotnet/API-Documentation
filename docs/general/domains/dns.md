DNS
=============

*Access Levels*    
__Group:__ general, domains     
__Resource:__ dns

List all DNS records
-------------------

```php
GET 	https://api.create.net/dns
```

### Input

```php
GET 	https://api.create.net/dns?domain_id=2672
```

* *domain_id* - ID of domain [int]
@TODO

### Response

```console
Status: 200 OK
```

```json
{ "mail_alias" :[ 
	{
		"ID" : "236",
		"ADD DATA" : "ADD DATA"
	}
]}
```

Get a single DNS record
-----------------------

```php
GET 	https://api.create.net/dns/:id
```

### Response

```console
Status: 200 OK
```

```json
{ "mail_alias" : 
	{
		"ID" : "236",
		"ADD DATA" : "ADD DATA"
	}
}
```

Create a DNS record
------------------

```php
POST 	https://api.create.net/dns
```

### Input

@TODO

### Response

```console
Status: 201 Created
Location: http://api.create.net/dns/236
```

```json
{ "mail_alias" : 
	{
		"ID" : "236",
		"ADD DATA" : "ADD DATA"
	}
}
```

Update a DNS record
------------------

```php
PUT 	https://api.create.net/dns/:id
```

### Input

@TODO

### Response

```console
Status: 200 OK
```

Delete a DNS record
------------------

```php
DELETE 	https://api.create.net/dns/:id
```

### Response

```console
Status: 200 OK
```