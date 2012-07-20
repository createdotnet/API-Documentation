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