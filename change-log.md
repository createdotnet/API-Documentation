---
layout: default
title: Change Log
---

# Change Log

### 16th November 2015
* Implement sort_property and sort_direction.
* Add the average_rating property to Products model.

### 12th November 2015
* Added documentation for sorting of records.

### 10th November 2015
* Added 'visible' property to Products model.
* Implemented the full Shop Customers model - [see docs](/API-Documentation/resources/shop/customers.html).

### 16th September 2015
* Implemented Apps and consequently updated authentication requirements
* Added documentation for creating Apps

### 13th August 2015
* Changed how versioning works, version is now sent as an HTTP header "X-Version", [see docs](/API-Documentation/get-started.html).
* Changed authentication token name to "X-Token" as not to conflict with official HTTP Headers.

### 23rd July 2015
* Added the Customers model
* Updated documentation to not include non-live models

## v0 -> v1

### 11th June 2015 Noun Container Object
The structure now accurately represents the correct data model by containing the data in an object. For instance a list of products are now contained in a `products` object at the root of the JSON response. An individual item is contained in a singular noun i.e. `product`.

See the documentation for details; [Products](/API-Documentation/resources/shop/products_and_categories/products.html)
