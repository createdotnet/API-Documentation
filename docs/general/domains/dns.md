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
GET 	https://api.create.net/dns?domain_id=2672&type=MX
```

* *domain_id* - ID of domain [int]
* *type* - type of DNS record ['NS','MX','A','CNAME']
@TODO

### Response

```console
Status: 200 OK
```

```json
{ "dns" :[ 
	{
		"id" : "242223",
		"domain_id" : "226216",
		"name" : "lifefloat.co.uk",
		"type" : "MX",
		"content" : "mail.create.net",
		"ttl" : "900",
		"prio" : "10",
		"change_date: : ""
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
{ "dns" : 
	{
		"id" : "242223",
		"domain_id" : "226216",
		"name" : "lifefloat.co.uk",
		"type" : "MX",
		"content" : "mail.create.net",
		"ttl" : "900",
		"prio" : "10",
		"change_date: : ""
	}
}
```

Create a DNS record
------------------

```php
POST 	https://api.create.net/dns
```

### Input

* *domain_id* Required [int]
* *name* Required [string]
* *type* Required ['NS','MX','A','CNAME']
* *content* Required [string]

### Response

```console
Status: 201 Created
Location: http://api.create.net/dns/242823
```

```json
{ "dns" : 
	{
		"id" : "242823",
		"domain_id" : "226216",
		"name" : "www.lifefloat.co.uk",
		"type" : "CNAME",
		"content" : "lifefloat.co.uk",
		"ttl" : "900",
		"prio" : "0",
		"change_date: : ""
	}
}
```

Update a DNS record
------------------

```php
PUT 	https://api.create.net/dns/:id
```

### Input

* *name* Required [string]
* *type* Required ['NS','MX','A','CNAME']
* *content* Required [string]

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