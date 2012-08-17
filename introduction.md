---
layout: default
title: Introduction
---

# Introduction

API access is over HTTPS and available from api.create.net. Our API currently only supports JSON. Authentication is handled with OAuth2

The standard four HTTP verbs are used to access our resources:

*GET* - Use when requesting an existing resource

*POST* - Use when creating a new resource

*PUT* - Use when updating an existing resource

*DELETE* - Use when deleting a resource

## About Request and Response Formats

Requests and responses can be provided in JSON. Set the HTTP Accept header to specify the response format and the HTTP Content-Type header to specify the request format.

JSON 

{% highlight php %}
Accept: application/json
Content-Type: application/json
{% endhighlight %}

## Access Levels

Access to our resources is limited by user permissions. Resources are split into groups, you can request access to a whole group, or individual resources within a group. The minimum required access level is specified for each resource. The access levels are as follows:

{% highlight php %}
- general
	- site_details
		- account_details
		- account_stats  
	- domains
		- domain_names
		- mail_alias
		- dns
	- website_stats  
- content  
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
- shop
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
{% endhighlight %}

## Pagination

API requests that returns multiple items, such as listing orders, will be paginated (default to 25 items per page). In order to alter the number of records returned per page, a client can provide the per_page param (limited to 100 items per page). 

To retrieve the next set of data, you can provide the last_id param. This would be the last ID of the previous page, or an ID to offset the request.

{% highlight php %}
GET		/orders?last_id=45546=5&per_page=50
{% endhighlight %}