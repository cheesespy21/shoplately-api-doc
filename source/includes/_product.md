# Product

## Get All Products

```shell
curl "http://shoplately.com/api/v1/products" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 198378,
    "groupDealId": 8625,
    "companyId": 211,
    "title": "Spring Buds Necklace",
    "limitNum": 20,
    "soldNum": 4,
    "retailPrice": 0,
    "salePrice": 19,
    "everyDayPrice": 19,
    "shippingPrice": "0.00",
    "flatShippingEnabled": 1,
    "createdTime": 1388702170,
    "soldOutTime": 0,
    "gift": 0,
    "maxPurchase": 1,
    "numOption": 2,
    "companyDomain": "",
    "handlingDays": 1,
    "sku": "211-8625-198378",
    "deleted": 0,
    "published": true,
    "productId": 0,
    "backInStock": 0,
    "ranking": 17,
    "views": 6,
    "numFavorites": 0,
    "categoryId": 47,
    "groupStaging": 0,
    "publishedTime": 1389626724,
    "lastPublishedTime": 1389626724,
    "options": {
      "310737": {
        "id": 310737,
        "flashDealId": 198378,
        "limitNum": 10,
        "soldNum": 3,
        "leftNum": 7,
        "quantity": 7,
        "soldOutTime": 0,
        "createdTime": 1388702170,
        "ranking": 0,
        "type": 0,
        "sku": "LW-N9368-TQ",
        "deleted": 0,
        "optionDetailId1": 489114,
        "optionDetailId2": 489117,
        "optionDetail1": {
          "id": 489114,
          "label": "One size",
          "title": "Size",
          "flashOptionDetailImgId": 0,
          "isDefault": 0,
          "type": 1
        },
        "optionDetail2": {
          "id": 489117,
          "label": "Turquoise",
          "title": "Color",
          "flashOptionDetailImgId": 0,
          "isDefault": 1,
          "type": 2
        },
        "companyId": 211,
        "optionDesc": "Turquoise"
      },
      "310740": {
        "id": 310740,
        "flashDealId": 198378,
        "limitNum": 10,
        "soldNum": 1,
        "leftNum": 9,
        "quantity": 9,
        "soldOutTime": 0,
        "createdTime": 1388702170,
        "ranking": 1,
        "type": 0,
        "sku": "LW-N9368-YL",
        "deleted": 0,
        "optionDetailId1": 489114,
        "optionDetailId2": 489120,
        "optionDetail1": {
          "id": 489114,
          "label": "One size",
          "title": "Size",
          "flashOptionDetailImgId": 0,
          "isDefault": 0,
          "type": 1
        },
        "optionDetail2": {
          "id": 489120,
          "label": "Yellow",
          "title": "Color",
          "flashOptionDetailImgId": 0,
          "isDefault": 0,
          "type": 2
        },
        "companyId": 211,
        "optionDesc": "Yellow"
      }
    },
    "category": {
      "id": 47,
      "name": "Necklaces",
      "parentId": 19,
      "left": 4,
      "right": 5,
      "numProduct": 8604,
      "parentCateogries": [
        {
          "id": 19,
          "name": "Jewelry",
          "parentId": 18,
          "left": 3,
          "right": 22,
          "numProduct": 26638,
          "parentCateogries": [],
          "parentCategories": [],
          "urlRoute": "jewelry"
        },
        {
          "id": 18,
          "name": "Accessories",
          "parentId": 1,
          "left": 2,
          "right": 71,
          "numProduct": 32357,
          "parentCateogries": [],
          "parentCategories": [],
          "urlRoute": "accessories"
        },
        {
          "id": 1,
          "name": "All",
          "parentId": 0,
          "left": 1,
          "right": 178,
          "numProduct": 35069,
          "parentCateogries": [],
          "parentCategories": [],
          "urlRoute": "all"
        }
      ],
      "parentCategories": [
        {
          "id": 19,
          "name": "Jewelry",
          "parentId": 18,
          "left": 3,
          "right": 22,
          "numProduct": 26638,
          "parentCateogries": [],
          "parentCategories": [],
          "urlRoute": "jewelry"
        },
        {
          "id": 18,
          "name": "Accessories",
          "parentId": 1,
          "left": 2,
          "right": 71,
          "numProduct": 32357,
          "parentCateogries": [],
          "parentCategories": [],
          "urlRoute": "accessories"
        },
        {
          "id": 1,
          "name": "All",
          "parentId": 0,
          "left": 1,
          "right": 178,
          "numProduct": 35069,
          "parentCateogries": [],
          "parentCategories": [],
          "urlRoute": "all"
        }
      ],
      "urlRoute": "jewelry-necklaces"
    },
    "company": {
      "id": 211,
      "name": "LILY WANG",
      "vanityUrl": "shoplilywang",
      "domain": "shoplilywang",
      "website": "http://www.shoplilywang.com",
      "description": "Lily Wang is an online boutique based in Downtown Los Angeles.  We offer a hand curated selection of quality women's apparel and accessories for affordable prices.",
      "email": "INFO@SHOPLILYWANG.COM",
      "webImg": "",
      "promoCodeScreen": "",
      "websiteRedeem": "",
      "balance": "0.00",
      "supportEmail": "INFO@SHOPLILYWANG.COM",
      "techEmail": "INFO@SHOPLILYWANG.COM",
      "billingEmail": "INFO@SHOPLILYWANG.COM",
      "feedbackTotal": 726,
      "feedbackRating": "4.5",
      "feedbackPercent": 90,
      "numFavorites": 12092,
      "createdTime": 1351544231,
      "facebookUrl": "https://www.facebook.com/lilywangshop",
      "twitterUrl": "https://twitter.com/shoplilywang",
      "level": 5,
      "lastSentTime": 0,
      "lastPublishedTime": 1419888237,
      "customDomain": "",
      "merchantMemo": "",
      "pinterestUrl": "http://pinterest.com/search/?q=shoplilywang",
      "instagramUrl": "http://www.instagram.com/shoplilywang",
      "returnPolicy": "Returns are super easy! You can submit a return request through Shoplately within 14 days after the item is received. We will gladly accept any unworn items with tags still on.",
      "bannedTime": 0,
      "managerUserId": 335006,
      "ranking": 0,
      "acquisition": 2,
      "modifiedTime": 1401892687,
      "managerReminder": 0,
      "companyImage": null
    },
    "flashPrice": 14,
    "type": "flash",
    "quantity": 16,
    "leftNum": 16,
    "url": "/product/198378/spring_buds_necklace",
    "numPriceOption": 1,
    "maxPurchaseGift": 0,
    "status": 1,
    "parentId": null,
    "endTime": 1389628800,
    "startTime": 1389024000,
    "expired": 0,
    "locked": 0,
    "parentUrl": "/group/shoplilywang/8625",
    "groupDeal": {
      "id": 8625,
      "companyId": 211,
      "level": 1,
      "title": "NEW YEAR NEW YOU: Great New Items On Sale",
      "subTitle": "",
      "createdTime": 1388507662,
      "startTime": 1389024000,
      "endTime": 1389628800,
      "soldOutTime": 0,
      "expired": 1,
      "permanentUrl": "shoplilywang/8625",
      "soldNum": 0,
      "numProduct": 40,
      "companyBillingStatus": 0,
      "comission": "0.15",
      "enrolling": 0,
      "deleted": 0,
      "locked": 0,
      "featured": 1,
      "type": "group",
      "flags": 0,
      "shippingPrice": "0.00",
      "specialInstruction": "",
      "defaultSort": 1,
      "shorterTitle": "NEW YEAR NEW YOU: Great New Items On Sale",
      "running": false,
      "durationDay": 7,
      "url": "/group/shoplilywang/8625",
      "metaType": "group",
      "companyItems": null,
      "totalItems": null,
      "companySold": null,
      "originalType": 0
    },
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
    "groupDealAddTime": 1388702170,
    "sizeChartId": 0,
    "feedbackRating": "0.0",
    "feedbackTotal": 0,
    "flags": 0,
    "shipsInMin": 0,
    "shipsInMax": 0
  }
]
```

This endpoint retrieves all products.

### HTTP Request

`GET /api/v1/products`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
limit | 25 | The number of products to be retrieved
page | 1 | page number


## Get a Specific Product

```shell
curl "http://shoplately.com/api/v1/products/<ID>" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json

```

This endpoint retrieves a specific product.

### HTTP Request

`GET /api/v1/products/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the product

## Upload a New Product

```shell
curl -XPOST "http://shoplately.com/api/v1/products" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow" \
  -H "Content-Type: application/json" \
  -d '[
        {
          "title": "Spring Buds Necklace",
          "salePrice": 19,
          "quantity": 0,
          "everyDayPrice": 19,
          "shippingPrice": "0.00",
          "sku": "211-8625-198378",
          "material": "- Metal.",
          "measurement": "- About 18\" in length, 2\" extender.",
          "description": "- Color: Comes in Bright yellow; Turquoise.\n- Lobster clasp closure.\n- Lead and nickel safe."
          "categoryId": 47,
          "size" : [
            "small",
            "large"
          ],
          "options": {
            "type": "color",
            "option": [
              {
                "label": "Turquoise",
                "images": [
                  "http://imageserver.com/a.jpg",
                  "http://imageserver.com/b.jpg",
                  "http://imageserver.com/c.jpg"
                ]
              },
              {
                "label": "Yellow",
                "images": [
                  "http://imageserver.com/d.jpg",
                  "http://imageserver.com/e.jpg",
                  "http://imageserver.com/f.jpg"
                ]
              }
            ]
          },
          "optionSku": [
            "SMALL-TURQUOISE",
            "SMALL-YELLOW",
            "LARGE-TURQUOISE",
            "LARGE-YELLOW"
          ],
          optionQuantity: [
            5,
            5,
            4,
            4
          ]
        },
        {...}
      ]'
```

> The above command returns JSON structured like this:

```json
{
  "id": 134241
  ???
}

```

This endpoint upload products.

### HTTP Request

`POST /api/v1/products`

### JSON fields

Parameter | Description
--------- | -----------
ID | The ID of the product
???

## Update Product Info

Change price of the products

### HTTP Request

`PUT /api/v1/products/<ID>`

### fields
Parameter | Description
--------- | -----------
<ID> | The ID of the product
salePrice | new sale price
everyDayPrice | new every day price

## Update Option Quantity

<aside class="notice">We don't update quantity of products but options since quantity is bound to options.</aside>

### HTTP Request

`PUT /api/v1/options/<ID>`

### fields
Parameter | Description
--------- | -----------
<ID> | The ID of an option to be updated
quantity | new quantity


## Out of stock

Change quantity of a product to 0 (including all options)

### HTTP Request

`DELETE /api/v1/products/<ID>/stock`

