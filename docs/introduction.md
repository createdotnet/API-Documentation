# Introduction

All API access is over HTTPS and accessded from api.create.net. JSON and XML formats are supported. Users can authenticate Apps using OAuth 2.0

Four HTTP verbs are used to access resources:

*GET* - Use when requesting an existing resource

*POST* - Use when creating a new resource

*PUT* - Use when updating an existing resource

*DELETE* - Use when deleting a resource

## About Request and Response Formats

Requests and responses can be provided in either JSON or XML. Set the HTTP Accept header to specify the response format and the HTTP Content-Type header to specify the request format. If none is set, the default will be JSON.

JSON 

```php
Accept: application/json
Content-Type: application/json
```

XML

```php
Accept: application/xml
Content-Type: application/xml
```

## Access Levels

Access to Create resources is limited by user permissions. Resources are split into groups, you can request access to a whole group, or individual resources within a group. The minimum required access level is specified for each resource. The access levels are as follows:

```ruby
General
	- Site Details
		- Account Details
		- Account Stats
	- Domains
		- Domains
		- Mail Alias
		- DNS
	- Website Stats

Content
	- Pages
	- Blogs
		- Blog
		- Blog Comments
	- Guestbooks
	- Custom forms
	- Widgets
	- Event calendars
	- Html Fragments
	- Enquires

Shop
	- Products & Categories
		- Products
		- Categories
	- Stock Control
	- Product Options
	- Orders
		- Orders
		- Disptach Notes 
		- Address Labels
		- Order Status
	- Postage & Tax
	- Payment Gateways
	- Shop Sale
	- Customer Accounts
	- Import/Export
		- Import
		- Export
	- Downloadables
	- Discount Codes
	- Product Search
	- Shop Reports
		- Financial Reports
		- Product Reports
```

### Internal Access

```ruby
0 : Application
1 : Admin
2 : Reporting
```


## Pagination

API requests that returns multiple items, such as listing one of the resources, will be paginated (default to 25 items per page). A client can retrieve a specific page by providing the page param. In order to alter the number of records returned per page, a client can provide the per_page param (limited to 100 items per page).

```php
GET		/orders?page=5&per_page=50
```