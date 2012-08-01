Enquires
=============

*Access Levels*    
__Group:__ content     
__Resource:__ enquires

List all enquires
-------------------

```php
GET 	https://api.create.net/enquirys
```

### Input

```php
GET 	https://api.create.net/enquirys?datetime_from=2010-04-07%2018:08:14
```
* *datetime_from* - Date and Time of from range [2010-04-07 18:08:14]
* *datetime_to* - Date and Time of to range [2012-06-02 00:00:00]

### Response

```console
Status: 200 OK
```

```json
{ "enquirys" :[
	{
		"ID" : "355766",
		"sender" : "adam@create.net",
		"subject" : "Recent order",
		"message" : "Thanks for the order, I\'m impressed with the quality. Do you also have it in Blue?",
		"datestamp" : "2012-05-16 15:17:04"
	}
]}
```

Get a single enquiry
-------------------------

```php
GET 	https://api.create.net/enquirys/:id
```

### Response

```console
Status: 200 OK
```

```json
{ "enquirys" :
	{
		"ID" : "355766",
		"sender" : "adam@create.net",
		"subject" : "Recent order",
		"message" : "Thanks for the order, I\'m impressed with the quality. Do you also have it in Blue?",
		"datestamp" : "2012-05-16 15:17:04"
	}
}
```


Delete an enquiry
------------------

```php
DELETE 	https://api.create.net/enquirys/:id
```

### Response

```console
Status: 200 OK
```