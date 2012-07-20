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

Access to Create resources is limited by user permissions. The minimum required access level is specified for each resource. The access levels are as follows:

```ruby
0 : No Access
1 : Static Content, Read Only
2 : Static Content, Full Access
3 : Shop Content, Read Only
4 : Shop Content, Full Access
5 : All Content, Read Only
6 : All Content, Full Access
```

## Pagination

API requests that returns multiple items, such as listing one of the resources, will be paginated (default to 25 items per page). A client can retrieve a specific page by providing the page param. In order to alter the number of records returned per page, a client can provide the per_page param (limited to 100 items per page).

```php
GET		/orders?page=5&per_page=50
```