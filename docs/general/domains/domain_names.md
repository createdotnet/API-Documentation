Domain names
=============

*Access Levels*    
__Group:__ general, domains     
__Resource:__ domain_names

List all domain names
-------------------

```php
GET 	https://api.create.net/domain_names
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
		"ID" : "228025",
		"domain" : "beachfile2.co.uk",
		"date_registered" : "2012-07-17",
		"date_expire" : "2014-07-17",
		"isprimary" : "1",
		"isourdns" : "1"
	}
]}
```

Get a single domain name
-----------------------

```php
GET 	https://api.create.net/domain_names/:id
```

### Response

```console
Status: 200 OK
```

```json
{ "domain_name" : 
	{
		"ID" : "228025",
		"domain" : "beachfile2.co.uk",
		"date_registered" : "2012-07-17",
		"date_expire" : "2014-07-17",
		"isprimary" : "1",
		"isourdns" : "1"
	}
}
```

Delete a domain name
------------------

```php
DELETE 	https://api.create.net/domain_names/:id
```

### Response

```console
Status: 200 OK
```