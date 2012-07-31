Account details
=============

*Access Levels*    
__Group:__ general, site_details     
__Resource:__ account_details

List account details
-------------------

```php
GET 	https://api.create.net/account_details
```

### Response

```console
Status: 200 OK
```

```json
{ "account_details" :
	{
		"ID" : "73663",
		"userid" : "537",
		"company_name" : "Smiths Sweet Emporium",
		"site_name" : "Smiths Amazing Sweets",
		"address1" : "291 Albert Road",
		"address2" : "",
		"town" : "Brighton",
		"county" : "East Sussex",
		"postcode" : "BN2 4QN",
		"country" : "United Kindom"
		"telephone" : "01273 431234",
		"email" : "adam@smithssweets.net",
		"creation_date" : "2002-06-19 14:18:46",
		"account_type_INC" : "Pro Seller",
		"payment_due_date" : "2014-06-12"
	}
}
```

Update account_details
------------------

```php
PUT 	https://api.create.net/account_details
```

### Input

* *company_name* [string]
* *site_name* [string]
* *address1* [string]
* *address2* [string]
* *town* [string]
* *county [string]
* *postcode [string]
* *country [string]
* *telephone [string]
* *email [string]

### Response

```console
Status: 200 OK
```