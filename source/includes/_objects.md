# Objects

## Users

### User Object
Name | Type | Description
---- | ---- | -----------
userId | int | User ID
name | string | Full name
image | string | Absolute URL of user image
createdTime | int | UNIX timestamp of user creation time

### Company Object
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

### ShippingAddress Object
Name | Type | Description
---- | ---- | -----------
shippingAddressId | int | Shipping Address ID
firstName | string | First name
lastName | string | Last name
addressLine1 | string | Address line 1
addressLine2 | string | Address line 2
city | string | City
state | string | State (2-letter abbreviation)
zipCode | string | ZIP code
zipCodeExt | string | ZIP code extension
phoneNumber | string | Phone number

## Products

### Product Object
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

### Option Object
Name | Type | Description
---- | ---- | -----------
optionId | int | Option ID
name | string | Option name
sku | string | SKU of option
details | array | Option detail objects
quantity | int | Available quantity of this option
sold | int | Total sold of this option
images | array | Absolute image URLs
isSoldOut | bool | If the option is currently sold out
createdTime | int | UNIX timestamp of option creation time
soldOutTime | int | UNIX timestamp of option sellout time

### OptionDetail Object
Name | Type | Description
---- | ---- | -----------
optionDetailId | int | Option detail ID
type | string | Option detail type (e.g. "Size", "Color")
name | string | Option detail name (e.g. "Small", "Blue")

### Category Object
<aside class="notice">
The top-most parent will have <strong>null</strong> as its parent value.
</aside>

Name | Type | Description
-----|------|------------
categoryId | int | Category ID
name | string | Category name
url | string | Absolute URL of the category page
parentId | int | id of Parent category
children | Category[] | array of children categories

### SaleEvent Object
Name | Type | Description
---- | ---- | -----------
saleEventId | int | Sale event ID
name | string | Sale event name
url | string | Absolute URL of the sale event page
startTime | int | UNIX timestamp of sale start
endTime | int | UNIX timestamp of sale end
createdTime | int | UNIX timestamp of sale event creation time

## Purchases

### Purchase Object
Name | Type | Description
---- | ---- | -----------
purchaseId | int | Purchase ID
user | object | User object
shippingAddress | object | Shipping address
details | array | Purchase detail objects
refunds | array | Refund objects
subtotal | float | Purchase subtotal (sum of all item prices * quantity)
shipping | float | Total shipping amount
tax | float | Total amount of tax collected
ccPrice | float | Amount captured from the credit card
creditPrice | float | Amount of SL credit applied toward this purchase
taxRate | float | Tax rate used
taxCountyName | string | Tax county name
taxCountyNumber | int | Tax county number
isShippingTaxable | bool | If the shipping costs are taxable
isPending | bool | If the purchase has not been successfully charged yet
isCanceled | bool | If the purchase has been fully canceled and refunded
createdTime | int | UNIX timestamp of purchase creation time

### PurchaseDetail Object
Name | Type | Description
---- | ---- | -----------
purchaseDetailId | int | Purchase detail ID
product | object | Product object
shipment | object | Shipment object
quantity | int | Total quantity ordered
unitPrice | float | Unit price
price | float | Total price
tax | float | Amount of tax collected
isCanceled | bool | If the item(s) have been canceled and refunded
isShipped | bool | If the item(s) have been shipped
isDelivered | bool | If the item(s) have been delivered
quantityReturned | int | Total quantity returned

### Shipment Object
Name | Type | Description
---- | ---- | -----------
shipmentId | int | Shipment ID
shipmentProvider | string | Shipment provider
shipmentType | string | Shipment type
trackingNumber | string | Shipment tracking number
weight | float | Shipment weight
volume | float | Shipment volume
price | float | Total shipping price
shippedTime | int | UNIX timestamp of ship time
deliveredTime | int | UNIX timestamp of delivered time

### Refund Object
Name | Type | Description
---- | ---- | -----------
refundId | int | Refund ID
productRefund | float | Product refund amount
otherRefund | float | Other refund amount
totalRefund | float | Total refund amount
refundTime | int | UNIX timestamp of refund time

## Customer Service

### Thread Object
Name | Type | Description
---- | ---- | -----------
threadId | int | Thread ID
to | object | ThreadAuthor object
from | object | ThreadAuthor object
subject | string | Thread subject
purchase | object | Purchase (if applicable)
messages | array | Thread message objects
createdTime | int | UNIX timestamp of thread creation time

### ThreadAuthor Object
Name | Type | Description
---- | ---- | -----------
details | object | User or Company object
isCompany | bool | If this participant is a company
isAdmin | bool | If this participant is an admin

### ThreadMessage Object
Name | Type | Description
---- | ---- | -----------
messageId | int | Thread message ID
author | object | ThreadAuthor object
message | string | Message body
createdTime | int | UNIX timestamp of message creation time

