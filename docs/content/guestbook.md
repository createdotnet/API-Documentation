Guestbook
=============

*Access Levels*    
__Group:__ content     
__Resource:__ guestbook

List all guestbook entries
--------------------------

```php
GET 	https://api.create.net/guestbook
```

### Input

```php
GET 	https://api.create.net/guestbook?datetime_from=2010-04-07%2018:08:14
```
* *datetime_from* [2010-04-07 18:08:14]
* *datetime_to* [2012-06-02 00:00:00]
* *approved* [int]

### Response

```console
Status: 200 OK
```

```json
{ "guestbook" :[
	{
		"ID" : "1743",
		"name" : "Adam",
		"email" : "adam@create.net",
		"website" : "lmgtfy.com",
		"message" : "Thanks for the advice on the fabric colour, it matched perfectly."
		"datestamp" : "2008-09-08 19:08:21"
		"approved" : "1"
	}
]}
```

Get a single guestbook entry
----------------------------

```php
GET 	https://api.create.net/guestbook/:id
```

### Response

```console
Status: 200 OK
```

```json
{ "guestbook" :
	{
		"ID" : "1743",
		"name" : "Adam",
		"email" : "adam@create.net",
		"website" : "lmgtfy.com",
		"message" : "Thanks for the advice on the fabric colour, it matched perfectly."
		"datestamp" : "2008-09-08 19:08:21"
		"approved" : "1"
	}
}
```


Delete a guestbook entry
------------------------

```php
DELETE 	https://api.create.net/guestbook/:id
```

### Response

```console
Status: 200 OK
```	