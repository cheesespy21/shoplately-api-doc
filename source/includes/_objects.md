# Objects

## Product Object
Name | Type | Description
---- | ---- | -----------
productId | int | Product ID
name | string | Product name
description | string | Product description
material | string | Product material description
measurement | string | Product measurement description
company | object | Company object
saleEvent | object | Sale event object
category | object | Parent category object
options | array | Option objects
quantity | int | Available quantity across all options
sold | int | Total sold across all options
price | float | Current price
regularPrice | float | The regular price (used for comparison when the product is on sale)
views | int | Number of views this product has received
url | string | Absolute URL of the product page
isBackInStock | bool | If the product was recently restocked
isDeleted | bool | If the product is deleted
isOnSale | bool | If the product is currently on sale
isPublished | bool | If the product is published
isSoldOut | bool | If the product is currently sold out
createdTime | int | UNIX timestamp of product creation time
publishedTime | int | UNIX timestamp of first product publish time
lastPublishedTime | int | UNIX timestamp of most recent product publish time

## Company Object
Name | Type | Description
---- | ---- | -----------
companyId | int | Company ID
name | string | Company name
website | string | External company website
description | string | Company description
email | string | Company general contact e-mail
supportEmail | string | Company support e-mail
techEmail | string | Company technical contact e-mail
billingEmail | string | Company billing e-mail
createdTime | int | UNIX timestamp of company creation time

## SaleEvent Object
Name | Type | Description
---- | ---- | -----------
saleEventId | int | Sale event ID
name | string | Sale event name
url | string | Absolute URL of the sale event page
startTime | int | UNIX timestamp of sale start
endTime | int | UNIX timestamp of sale end
createdTime | int | UNIX timestamp of sale event creation time

## Category Object
<aside class="notice">
The top-most parent will have <strong>null</strong> as its parent value.
</aside>

Name | Type | Description
-----|------|------------
categoryId | int | Category ID
name | string | Category name
url | string | Absolute URL of the category page
parent | object | Parent category object

## Option Object
Name | Type | Description
---- | ---- | -----------
optionId | int | Option ID
name | string | Option name
sku | string | SKU of option
details | array | Option detail objects
quantity | int | Available quantity of this option
sold | int | Total sold of this option
isSoldOut | bool | If the option is currently sold out
createdTime | int | UNIX timestamp of option creation time
soldOutTime | int | UNIX timestamp of option sellout time

## OptionDetail Object
Name | Type | Description
---- | ---- | -----------
optionDetailId | int | Option detail ID
type | string | Option detail type (e.g. "Size", "Color")
name | string | Option detail name (e.g. "Small", "Blue")
images | array | Absolute image URLs
