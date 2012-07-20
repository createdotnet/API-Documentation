Domain mail alias
=============

*Access Levels*    
__Group:__ general, domains     
__Resource:__ mail_alias

List all mail alias
-------------------

```php
GET 	https://api.create.net/domain/mail_alias
```

### Input

```php
GET 	https://api.create.net/domain/mail_alias?domain_id=2672
```

* *domain_id* - ID of domain [int]

### Response

```console
Status: 200 OK
```

```json
{ "mail_alias" :[ 
	{
		"ID" : "236",
		"domain_id" : "2672",
		"alias" : "help",
		"email" : "adam@create.net"
	}
]}
```

Get a single mail alias
-----------------------

```php
GET 	https://api.create.net/domain/mail_alias/:id
```

### Response

```console
Status: 200 OK
```

```json
{ "mail_alias" : 
	{
		"ID" : "236",
		"domain_id" : "2672",
		"alias" : "help",
		"email" : "adam@create.net"
	}
}
```

Create a mail alias
------------------

```php
POST 	https://api.create.net/domain/mail_alias
```

### Input

* *domain_id* Required [int]
* *alias* Required [string]
* *email* Required [string]

### Response

```console
Status: 201 Created
Location: http://api.create.net/domain/mail_alias/236
```

```json
{ "mail_alias" : 
	{
		"ID" : "236",
		"domain_id" : "2672",
		"alias" : "help",
		"email" : "adam@create.net"
	}
}
```

Update a mail alias
------------------

```php
PUT 	https://api.create.net/domain/mail_alias/:id
```

### Input

ID, domain_id, alias, email

* *alias* [string]
* *email* Forwarding address [string]

### Response

```console
Status: 200 OK
```

Delete a mail alias
------------------

```php
DELETE 	https://api.create.net/domain/mail_alias/:id
```

### Response

```console
Status: 200 OK
```