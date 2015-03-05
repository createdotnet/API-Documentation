---
layout: default
title: Account Details
---

*Access Levels*    
__Group:__ general, site_details     
__Resource:__ account_details

List account details
-------------------

{% highlight php %}
GET 	https://api.create.net/account_details
{% endhighlight %}

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}

{% highlight javascript %}
{ "account_details" :
	{
		"ID" : 73663,
		"userid" : 537,
		"company_name" : "Smiths Sweet Emporium",
		"site_name" : "Smiths Amazing Sweets",
		"address1" : "291 Albert Road",
		"address2" : "",
		"town" : "Brighton",
		"county" : "East Sussex",
		"postcode" : "BN2 4QN",
		"country" : "United Kingdom"
		"telephone" : "01273 431234",
		"email" : "adam@smithssweets.net",
		"creation_date" : "2002-06-19 14:18:46",
		"package_name" : "Pro Seller",
		"payment_due_date" : "2014-06-12"
	}
}
{% endhighlight %}

Update account_details
------------------

{% highlight php %}
PUT 	https://api.create.net/account_details
{% endhighlight %}

### Input

<table>
	<thead>
		<tr>
			<th>Param</th>
			<th>Type</th>
			<th>Required</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>company_name</td>
			<td>string</td>
			<td>Optional</td>
			<td>The company name of the Create. account</td>
		</tr>
		<tr>
			<td>site_name</td>
			<td>string</td>
			<td>Optional</td>
			<td>The site name of the Create. account</td>
		</tr>
		<tr>
			<td>address1</td>
			<td>string</td>
			<td>Optional</td>
			<td>The first line of the account address</td>
		</tr>
		<tr>
			<td>address2</td>
			<td>string</td>
			<td>Optional</td>
			<td>The second line of the account address</td>
		</tr>
		<tr>
			<td>town</td>
			<td>string</td>
			<td>Optional</td>
			<td>The town of the account address</td>
		</tr>
		<tr>
			<td>county</td>
			<td>string</td>
			<td>Optional</td>
			<td>The county of the account address</td>
		</tr>
		<tr>
			<td>postcode</td>
			<td>string</td>
			<td>Optional</td>
			<td>The postcode of the account address</td>
		</tr>
		<tr>
			<td>country</td>
			<td>string</td>
			<td>Optional</td>
			<td>The country of the account address</td>
		</tr>
		<tr>
			<td>telephone</td>
			<td>string</td>
			<td>Optional</td>
			<td>The telephone number of the account address</td>
		</tr>
		<tr>
			<td>email</td>
			<td>string</td>
			<td>Optional</td>
			<td>The email address of the account address</td>
		</tr>
	</tbody>
</table>

### Response

{% highlight php %}
Status: 200 OK
{% endhighlight %}