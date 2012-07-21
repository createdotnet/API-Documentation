# Introduction

All API access is over HTTPS and accessded from api.create.net. JSON and XML formats are supported. Users can authenticate Apps using OAuth 2.0

Four HTTP verbs are used to access resources:

*GET* - Use when requesting an existing resource

*POST* - Use when creating a new resource

*PUT* - Use when updating an existing resource

*DELETE* - Use when deleting a resource

## About Request and Response Formats

Requests and responses can be provided in either JSON or XML. Set the HTTP Accept header to specify the response format and the HTTP Content-Type header to specify the request format.

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
general
	- site_details
		- account_details
		- account_stats
	- domains
		- domain_names
		- mail_alias
		- dns
	- website_stats

content
	- pages
	- blogs
		- blog_posts
		- blog_categories
		- blog_comments
	- guestbooks
	- custom_forms
	- widgets
	- event_calendars
	- html_fragments
	- enquires

shop
	- products_and_categories
		- products
		- categories
	- stock_control
	- product_options
	- orders_managment
		- orders
		- disptach_notes 
		- address_labels
		- order_status
	- postage_and_tax
	- payment_gateways
	- shop_sale
	- customer_accounts
	- import_export
		- import
		- export
	- downloadables
	- discount_codes
	- product_search
	- shop_reports
		- financial_reports
		- product_reports
```

### Internal Access

```ruby
Application  
Admin  
Reporting
```


## Pagination

API requests that returns multiple items, such as listing one of the resources, will be paginated (default to 25 items per page). A client can retrieve a specific page by providing the page param. In order to alter the number of records returned per page, a client can provide the per_page param (limited to 100 items per page).

```php
GET		/orders?page=5&per_page=50
```