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
    "id": 279270,
    "purchaseId": 114776,
    "userId": 164817,
    "dealId": 160121,
    "groupDealId": 8709,
    "optionId": 233129,
    "companyId": 211,
    "shippingId": 0,
    "flashShippingId": 0,
    "createdTime": 1421117728,
    "numPurchase": 1,
    "tax": "0.88",
    "totalPrice": "10.00",
    "status": 4,
    "type": "flash",
    "shippingPrice": "2.99",
    "numReturn": 0,
    "dealIds": 0,
    "optionIds": 0,
    "ids": 0,
    "returnId": 0,
    "returnRequestTime": 0,
    "returnReceivedTime": 0,
    "recommended": 0,
    "returnStatus": "",
    "deal": {
      "id": 160121,
      "groupDealId": 8709,
      "companyId": 211,
      "title": "Mystery Gift Box ($40 value)",
      "limitNum": 10,
      "soldNum": 1,
      "retailPrice": 0,
      "salePrice": 40,
      "everyDayPrice": 40,
      "shippingPrice": "0.00",
      "flatShippingEnabled": 1,
      "createdTime": 1382738442,
      "soldOutTime": 0,
      "gift": 0,
      "maxPurchase": 1,
      "numOption": 1,
      "companyDomain": "",
      "handlingDays": 1,
      "sku": "211-7430-160121",
      "deleted": 0,
      "published": true,
      "productId": 0,
      "backInStock": 0,
      "ranking": 3,
      "views": 0,
      "numFavorites": 0,
      "categoryId": 47,
      "groupStaging": 0,
      "publishedTime": 1419888237,
      "lastPublishedTime": 1419888237,
      "options": [],
      "category": null,
      "company": null,
      "flashPrice": 10,
      "type": "flash",
      "quantity": 9,
      "leftNum": 9,
      "url": "/product/160121/mystery_gift_box_value",
      "numPriceOption": 1,
      "maxPurchaseGift": 0,
      "status": 1,
      "parentId": null,
      "endTime": 1422460800,
      "startTime": 1419868800,
      "expired": 0,
      "locked": 0,
      "parentUrl": "/bash/jilliciouscharmsandaccessories/8709",
      "isEveryDayDeal": true,
      "isFlash": false,
      "isProduct": true,
      "isPick": false,
      "discount": 0,
      "clickInfo": null,
      "tags": null,
      "text": null,
      "featuredTime": 0,
      "images": null,
      "groupDealAddTime": 1382738442,
      "sizeChartId": 0,
      "feedbackRating": "0.0",
      "feedbackTotal": 0,
      "flags": 0,
      "shipsInMin": 0,
      "shipsInMax": 0
    },
    "option": {
      "id": 233129,
      "flashDealId": 160121,
      "limitNum": 10,
      "soldNum": 1,
      "leftNum": 9,
      "quantity": 9,
      "soldOutTime": 0,
      "createdTime": 1382738442,
      "ranking": 0,
      "type": 0,
      "sku": "Mystery Gift Box ($40 value)",
      "deleted": 0,
      "optionDetailId1": 382289,
      "optionDetailId2": 382292,
      "optionDetail1": {
        "id": 382289,
        "label": "One size",
        "title": "Size",
        "flashOptionDetailImgId": 0,
        "isDefault": 0,
        "type": 1
      },
      "optionDetail2": {
        "id": 382292,
        "label": "Default",
        "title": "Default",
        "flashOptionDetailImgId": 0,
        "isDefault": 1,
        "type": 11
      },
      "companyId": 211,
      "optionDesc": ""
    },
    "title": "Mystery Gift Box ($40 value)"
  }
]

```

This endpoint retrieves a specific product.

### HTTP Request

`GET /api/v1/orders`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
limit | 25 | The number of products to be retrieved
page | 1 | page number

## Confirm Shipping

```shell
curl -XPOST "http://shoplately.com/api/v1/orders/<id>/shipping" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow" \
  -H "Content-Type: application/json" \
  -d '{
        "date": "2015-08-11",
        "carrier": 3,
        "service": "First-Class Mail",
        "trackingNumber": "420591019101969010386840103308",
        "orders": [ 279270, ... ]
      }'
```

> The above command returns JSON structured like this:

```json
{
  ???
}

```


This endpoint retrieves a specific product.

### HTTP Request

`POST /api/v1/orders/<id>/shipping`

### JSON Parameters

## Cancel Order

refund, order id ???