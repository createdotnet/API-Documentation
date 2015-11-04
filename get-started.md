---
layout: default
title: Get Started
---

# Get Started

See latest updates on the [Change Log](/API-Documentation/change-log.html).

| Information ||
| ----------- ||
| Current API Version | `1` |
| API Protocol | HTTPS |
| API end point | `https://api.create.net/` |
| Response methods | JSON, JSONP |
| Authentication | Basic tokens |


The standard four REST verbs are used to access our resources:

| Method   | Purpose |
| -------- | ------- |
| *GET*    | Use when requesting an existing resource |
| *POST*   | Use when creating a new resource |
| *PUT*    | Use when updating an existing resource |
| *DELETE* | Use when deleting a resource |


## Getting Started

### Testing
You can easily get started testing the API using your Development API Token available within your Create account (Account > Developers & API)

{% highlight bash %}
curl -i -H "X-Token: <development-api-token>" -H "X-Version: 1" https://api.create.net/test
{% endhighlight %}

Development Tokens won't be able to be used in a production App however. You will need to create an [API App](#apps) and users will need to generate an Auth Token specifically for that App.

### Help Guides
* [Guide for Create Users](https://www.create.net/support/424-api-information-for-customers.html)
* [Guide for Developers](https://www.create.net/support/425-api-information-for-developers.html)

## Apps
Every request to the API must include your registered App Token in an HTTP Header 'X-AppToken'. Without this the API assumes that the Auth Token is a Development token.

You can create a new API App from your Create account;

1. Login to your Create account
2. Go to the 'Account' area in the top menu
3. Click on 'Developers & API'
4. Click Create App

Once you App has been created, you can generate an Auth Token by adding the App to the account's Connections. Continue reading for more information...

## Authentication

Auth Tokens are linked to a single Create account and API App, and must be sent with every api request as an HTTP Header called 'X-Token'.

You can generate a new Auth Token from your Create account;

1. Login to your Create account
2. Go to the 'Account' area in the top menu
3. Click on the 'Connections' link.
4. Click 'Add Account' and click on the required API App

You will now be provided with an Auth Token to be sent along side the App Token.

{% highlight php %}
X-Token=<auth-token>
X-AppToken=<app-token>
{% endhighlight %}

### Input with no token header

{% highlight php %}
GET 	https://api.create.net/test
{% endhighlight %}

### Response

{% highlight php %}
Status: 401 No authorisation token
{% endhighlight %}

{% highlight javascript %}
{
  "error": "No authorisation token"
}
{% endhighlight %}



## About Request and Response Formats

Requests and responses can be provided in JSON. Set the HTTP Accept header to specify the response format and the HTTP Content-Type header to specify the request format.

JSON

{% highlight php %}
Accept: application/json
Content-Type: application/json
{% endhighlight %}


JSONP

{% highlight php %}
Accept: application/javascript
X-JSONP-Callback: my_function_name
Content-Type: application/javascript
{% endhighlight %}

## Access Levels

** Currently not implemented **

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
		- order_products
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
