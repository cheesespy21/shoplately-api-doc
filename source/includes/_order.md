# Order

## Get All Orders

```shell
curl "http://shoplately.com/api/v1/orders" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
    {
        "purchaseId": 100,
        "user": {
            "userId": 100,
            "name": "Henry Jekyll",
            "image": null,
            "createdTime": 1234567890
        },
        "shippingAddress": {
        	"firstName": "Henry",
            "lastName": "Jekyll",
            "addressLine1": "123 Test St.",
            "addressLine2": "Apt. 99",
            "city": "San Jose",
            "state": "CA",
            "zipCode": "95126",
            "zipCodeExt": "",
            "phoneNumber": "123-456-7890"
        },
        "details": [
            {
                "purchaseDetailId": 100,
                "product": { ... },
                "shipment": {
                    "shipmentId": 100,
                    "trackingNumber": "ABCDEFGHIJK0123456789",
                    "shipmentProvider": "USPS",
                    "shipmentType": "First-Class Mail",
                    "weight": 0.19,
                    "volume": 70.13,
                    "shippedTime": 1234567890,
                    "deliveredTime": 1234567890
                },
                "quantity": 5,
                "unitPrice": 10,
                "price": 50,
                "tax": 4,
                "isCanceled": false,
                "isShipped": true,
                "isDelivered": true,
                "quantityReturned": 0
            }
        ],
        "refunds": [
            {
                "refundId": 8124,
                "productRefund": "18.99",
                "shippingRefund": "0.00",
                "otherRefund": "0.00",
                "totalRefund": "18.99",
                "refundTime": 1442216740
            }
        ],
        "subtotal": 50,
        "shipping": 5,
        "tax": 4,
        "ccPrice": 57,
        "creditPrice": 0,
        "taxRate": 0.08,
        "taxCountyName": "SANTA CLARA",
        "taxCountyNumber": 123,
        "isShippingTaxable": false,
        "isPending": false,
        "isCanceled": false,
        "createdTime": 1234567890
    },
    {
        "purchaseId": 200,
        "user": {
            "userId": 200,
            "name": "Edward Hyde",
            "image": null,
            "createdTime": 1234567890
        },
        "shippingAddress": {
        	"firstName": "Edward",
            "lastName": "Hyde",
            "addressLine1": "456 Test Ave.",
            "addressLine2": "",
            "city": "Los Angeles",
            "state": "CA",
            "zipCode": "90001",
            "zipCodeExt": "",
            "phoneNumber": "456-789-1011"
        },
        "details": [
            {
                "purchaseDetailId": 200,
                "product": { ... },
                "shipment": null,
                "quantity": 2,
                "unitPrice": 20,
                "price": 40,
                "tax": 0,
                "isCanceled": false,
                "isShipped": false,
                "isDelivered": false,
                "quantityReturned": 0
            }
        ],
        "refunds": [],
        "subtotal": 40,
        "shipping": 0,
        "tax": 0,
        "ccPrice": 57,
        "creditPrice": 0,
        "taxRate": 0,
        "taxCountyName": null,
        "taxCountyNumber": null,
        "isShippingTaxable": false,
        "isPending": false,
        "isCanceled": false,
        "createdTime": 1234567890
    }
]
```

This endpoint retrieves all orders.

### HTTP Request

`GET /api/v1/orders`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
pending | false | Include pending orders (orders that have not been fully charged yet)
canceled | false | Include canceled orders
page | 1 | Page number
limit | 25 | The number of orders to be retrieved


## Confirm Shipping

```shell
curl -XPOST "http://shoplately.com/api/v1/orders/200/shipping" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow" \
  -H "Content-Type: application/json" \
  -d '{
        "detailIds": [200],
        "date": 1234567890,
        "carrier": "USPS",
        "service": "First-Class Mail",
        "trackingNumber": "ABCDEFGHIJK0123456789"
      }'
```

> The above command returns JSON structured like this:

```json
{
    "purchaseId": 200,
    "user": {
        "userId": 200,
        "name": "Edward Hyde",
        "image": null,
        "createdTime": 1234567890
    },
    "shippingAddress": {
        "firstName": "Edward",
        "lastName": "Hyde",
        "addressLine1": "456 Test Ave.",
        "addressLine2": "",
        "city": "Los Angeles",
        "state": "CA",
        "zipCode": "90001",
        "zipCodeExt": "",
        "phoneNumber": "456-789-1011"
    },
    "details": [
        {
            "purchaseDetailId": 200,
            "product": { ... },
            "shipment": {
                "shipmentId": 200,
                "trackingNumber": "ABCDEFGHIJK0123456789",
                "shipmentProvider": "USPS",
                "shipmentType": "First-Class Mail",
                "weight": 0,
                "volume": 0,
                "shippedTime": 1234567890,
                "deliveredTime": 0
            },
            "quantity": 2,
            "unitPrice": 20,
            "price": 40,
            "tax": 0,
            "isCanceled": false,
            "isShipped": true,
            "isDelivered": false,
            "quantityReturned": 0
        }
    ],
    "refunds": null,
    "subtotal": 40,
    "shipping": 0,
    "tax": 0,
    "ccPrice": 57,
    "creditPrice": 0,
    "taxRate": 0,
    "taxCountyName": null,
    "taxCountyNumber": null,
    "isShippingTaxable": false,
    "isPending": false,
    "isCanceled": false,
    "createdTime": 1234567890
}
```

This endpoint marks specified purchase details as shipped.

### HTTP Request

`POST /api/v1/orders/<purchaseId>/shipping`

### URL Parameters
Name | Type | Description
---- | ---- | -----------
purchaseId | int | Purchase ID

### Payload
Name | Type | Description
---- | ---- | -----------
detailIds | array | Purchase detail IDs
shippedTime | int | UNIX timestamp of ship time
shipmentProvider | string | "USPS", "UPS" or "FedEx"
shipmentType | string | Shipment type
trackingNumber | string | Shipment tracking number


## Cancel Order

```shell
curl -XDELETE "http://shoplately.com/api/v1/orders/300" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
    "purchaseId": 200,
    "user": {
        "userId": 200,
        "name": "Edward Hyde",
        "image": null,
        "createdTime": 1234567890
    },
    "shippingAddress": {
        "firstName": "Edward",
        "lastName": "Hyde",
        "addressLine1": "456 Test Ave.",
        "addressLine2": "",
        "city": "Los Angeles",
        "state": "CA",
        "zipCode": "90001",
        "zipCodeExt": "",
        "phoneNumber": "456-789-1011"
    },
    "details": [
        {
            "purchaseDetailId": 200,
            "product": { ... },
            "shipment": null,
            "quantity": 2,
            "unitPrice": 20,
            "price": 40,
            "tax": 0,
            "isCanceled": true,
            "isShipped": false,
            "isDelivered": false,
            "quantityReturned": 0
        }
    ],
    "refunds": null,
    "subtotal": 40,
    "shipping": 0,
    "tax": 0,
    "ccPrice": 57,
    "creditPrice": 0,
    "taxRate": 0,
    "taxCountyName": null,
    "taxCountyNumber": null,
    "isShippingTaxable": false,
    "isPending": false,
    "isCanceled": true,
    "createdTime": 1234567890
}
```

### HTTP Request

`DELETE /api/v1/orders/<purchaseId>`

### URL Parameters
Name | Type | Description
---- | ---- | -----------
purchaseId | int | Purchase ID


