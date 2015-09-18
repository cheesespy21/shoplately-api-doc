# Product

## Get All Products

```shell
curl "https://api.lately.com/v1/products" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "productId": 1,
    "name": "My Awesome Product",
    "description": "My product is awesome",
    "material": "100% Awesome",
    "measurement": "Varies depending on option.",
    "quantity": 10,
    "sold": 5,
    "price": 20,
    "regularPrice": 25.99,
    "views": 100,
    "url": "https://shoplately.com/product/1/my-awesome-product",
    "isBackInStock": false,
    "isDeleted": false,
    "isOnSale": true,
    "isPublished": true,
    "isSoldOut": false,
    "createdTime": 1234567890,
    "publishedTime": 1234567890,
    "lastPublishedTime": 1234567890,
   
    "company": {
      "companyId": 1,
      "name": "My Awesome Company",
      "website": "http://www.example.com",
      "description": "My company is awesome!",
      "email": "example@example.com",
      "supportEmail": "example@example.com",
      "techEmail": "example@example.com",
      "billingEmail": "example@example.com",
      "createdTime": 1234567890
    },
    
    "saleEvent": {
      "saleEventId": 1,
      "name": "My Awesome Sale Event",
      "url": "https://shoplately.com/sale/1/my-awesome-sale-event",
      "startTime": 1234567890,
      "endTime": 1234567890,
      "createdTime": 1234567890
    },
    
    "category": {
      "categoryId": 2,
      "name": "Awesome Products",
      "url": "https://shoplately.com/category/awesome-products",
      "parent": {
        "categoryId": 1,
        "name": "All Products",
        "url": "https://shoplately.com",
        "parent": null
      }
    },
    
    "options": [
      {
        "optionId": 100,
        "name": "Small/Blue",
        "sku": "A-SMALL-BLUE",
        "quantity": 5,
        "sold": 3,
        "isSoldOut": false,
        "createdTime": 1234567890,
        "soldOutTime": null,
        "details": [
          {
            "optionDetailId": 100,
            "type": "Size",
            "name": "Small"
          },
          {
            "optionDetailId": 101,
            "type": "Color",
            "name": "Blue"
          }
        ],
        "images": [
          "https://shoplately.com/images/product/1/option/100/1.jpg",
          "https://shoplately.com/images/product/1/option/100/2.jpg"
        ]
      },
      {
        "optionId": 101,
        "name": "Large/Blue",
        "sku": "B-LARGE-BLUE",
        "quantity": 5,
        "sold": 2,
        "isSoldOut": false,
        "createdTime": 1234567890,
        "soldOutTime": null,
        "details": [
          {
            "optionDetailId": 102,
            "type": "Size",
            "name": "Large"
          },
          {
            "optionDetailId": 103,
            "type": "Color",
            "name": "Blue"
          }
        ],
        "images": [
          "https://shoplately.com/images/product/1/option/101/1.jpg",
          "https://shoplately.com/images/product/1/option/101/2.jpg"
        ]
      }
    ]
  },

  {
    "productId": 2,
    "name": "Your Awesome Product",
    "description": "Your product is awesome",
    "material": "100% Awesome",
    "measurement": "Varies depending on option.",
    "quantity": 10,
    "sold": 10,
    "price": 19.99,
    "regularPrice": 19.99,
    "views": 50,
    "url": "https://shoplately.com/product/2/your-awesome-product",
    "isBackInStock": false,
    "isDeleted": false,
    "isOnSale": false,
    "isPublished": true,
    "isSoldOut": true,
    "createdTime": 1234567890,
    "publishedTime": 1234567890,
    "lastPublishedTime": 1234567890,
   
    "company": {
      "companyId": 2,
      "name": "Your Awesome Company",
      "website": "http://www.example.com",
      "description": "Your company is awesome!",
      "email": "example@example.com",
      "supportEmail": "example@example.com",
      "techEmail": "example@example.com",
      "billingEmail": "example@example.com",
      "createdTime": 1234567890
    },
    
    "saleEvent": null,
    
    "category": {
      "categoryId": 2,
      "name": "Awesome Products",
      "url": "https://shoplately.com/category/awesome-products",
      "parent": {
        "categoryId": 1,
        "name": "All Products",
        "url": "https://shoplately.com",
        "parent": null
      }
    },
    
    "options": [
      {
        "optionId": 102,
        "name": "Small/Blue",
        "sku": "C-SMALL-BLUE",
        "quantity": 5,
        "sold": 5,
        "isSoldOut": true,
        "createdTime": 1234567890,
        "soldOutTime": 1234567890,
        "details": [
          {
            "optionDetailId": 104,
            "type": "Size",
            "name": "Small"
          },
          {
            "optionDetailId": 105,
            "type": "Color",
            "name": "Blue"
          }
        ],
        "images": [
          "https://shoplately.com/images/product/2/option/102/1.jpg",
          "https://shoplately.com/images/product/2/option/102/2.jpg"
        ]
      },
      {
        "optionId": 103,
        "name": "Large/Blue",
        "sku": "D-LARGE-BLUE",
        "quantity": 5,
        "sold": 5,
        "isSoldOut": true,
        "createdTime": 1234567890,
        "soldOutTime": 1234567890,
        "details": [
          {
            "optionDetailId": 106,
            "type": "Size",
            "name": "Large"
          },
          {
            "optionDetailId": 107,
            "type": "Color",
            "name": "Blue"
          }
        ],
        "images": [
          "https://shoplately.com/images/product/2/option/103/1.jpg",
          "https://shoplately.com/images/product/2/option/103/2.jpg"
        ]
      }
    ]
  }
]

```

This endpoint retrieves all products.

### HTTP Request

`GET /api/v1/products`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
unpublished | false | Include unpublished products
deleted | false | Include deleted products
page | 1 | Page number
limit | 25 | The number of products to be retrieved


## Get a Specific Product

```shell
curl "https://api.lately.com/v1/products/1" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "productId": 1,
  "name": "My Awesome Product",
  "description": "My product is awesome",
  "material": "100% Awesome",
  "measurement": "Varies depending on option.",
  "quantity": 10,
  "sold": 5,
  "price": 20,
  "regularPrice": 25.99,
  "views": 100,
  "url": "https://shoplately.com/product/1/my-awesome-product",
  "isBackInStock": false,
  "isDeleted": false,
  "isOnSale": true,
  "isPublished": true,
  "isSoldOut": false,
  "createdTime": 1234567890,
  "publishedTime": 1234567890,
  "lastPublishedTime": 1234567890,
 
  "company": {
    "companyId": 1,
    "name": "My Awesome Company",
    "website": "http://www.example.com",
    "description": "My company is awesome!",
    "email": "example@example.com",
    "supportEmail": "example@example.com",
    "techEmail": "example@example.com",
    "billingEmail": "example@example.com",
    "createdTime": 1234567890
  },
  
  "saleEvent": {
    "saleEventId": 1,
    "name": "My Awesome Sale Event",
    "url": "https://shoplately.com/sale/1/my-awesome-sale-event",
    "startTime": 1234567890,
    "endTime": 1234567890,
    "createdTime": 1234567890
  },
  
  "category": {
    "categoryId": 2,
    "name": "Awesome Products",
    "url": "https://shoplately.com/category/awesome-products",
    "parent": {
      "categoryId": 1,
      "name": "All Products",
      "url": "https://shoplately.com",
      "parent": null
    }
  },
  
  "options": [
    {
      "optionId": 100,
      "name": "Small/Blue",
      "sku": "A-SMALL-BLUE",
      "quantity": 5,
      "sold": 3,
      "isSoldOut": false,
      "createdTime": 1234567890,
      "soldOutTime": null,
      "details": [
        {
          "optionDetailId": 100,
          "type": "Size",
          "name": "Small"
        },
        {
          "optionDetailId": 101,
          "type": "Color",
          "name": "Blue"
        }
      ],
      "images": [
        "https://shoplately.com/images/product/1/option/100/1.jpg",
        "https://shoplately.com/images/product/1/option/100/2.jpg"
      ]
    },
    {
      "optionId": 101,
      "name": "Large/Blue",
      "sku": "B-LARGE-BLUE",
      "quantity": 5,
      "sold": 2,
      "isSoldOut": false,
      "createdTime": 1234567890,
      "soldOutTime": null,
      "details": [
        {
          "optionDetailId": 102,
          "type": "Size",
          "name": "Large"
        },
        {
          "optionDetailId": 103,
          "type": "Color",
          "name": "Blue"
        }
      ],
      "images": [
        "https://shoplately.com/images/product/1/option/101/1.jpg",
        "https://shoplately.com/images/product/1/option/101/2.jpg"
      ]
    }
  ]
}
```

This endpoint retrieves a specific product.

### HTTP Request

`GET /api/v1/products/<productId>`

### URL Parameters
Name | Type | Description
---- | ---- | -----------
productId | int | Product ID

## Upload a New Product

```shell
curl -XPOST "https://api.lately.com/v1/products" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow" \
  -H "Content-Type: application/json" \
  -d '{
        "name": "My Awesome New Product",
        "description": "This is new and awesome",
        "material": "100% Awesome",
        "measurement": "Tiny, but awesome.",
        "saleEventId": null,
        "categoryId": 2,
        "regularPrice": 19.99,
        "salePrice": 19.99,
        "optionDetail2Type": "Color",
        "options": [
          {
            "name": "Small/Blue",
            "sku": "MY-OWN-SKU-1",
            "quantity": 20,
            "details": {
              "Size": "Small",
              "Color": "Blue"
            },
            "images": [
              "http://www.example.com/products/my-external-image-1.jpg",
              "http://www.example.com/products/my-external-image-2.jpg"
            ]
          },

          {
            "name": "Large/Blue",
            "sku": "MY-OWN-SKU-2",
            "quantity": 20,
            "details": {
              "Size": "Large",
              "Color": "Blue"
            },
            "images": [
              "http://www.example.com/products/my-external-image-3.jpg",
              "http://www.example.com/products/my-external-image-4.jpg"
            ]
          }
        ]
      }'
```

> The above command returns JSON structured like this:

```json
{
  "productId": 3,
  "name": "My Awesome New Product",
  "quantity": 40,
  "sold": 0,
  "price": 19.99,
  "regularPrice": 19.99,
  "views": 0,
  "url": "https://shoplately.com/product/3/my-awesome-new-product",
  "isBackInStock": false,
  "isDeleted": false,
  "isOnSale": false,
  "isPublished": false,
  "isSoldOut": false,
  "createdTime": 1234567890,
  "publishedTime": null,
  "lastPublishedTime": null,
 
  "company": {
    "companyId": 1,
    "name": "My Awesome Company",
    "website": "http://www.example.com",
    "description": "My company is awesome!",
    "email": "example@example.com",
    "supportEmail": "example@example.com",
    "techEmail": "example@example.com",
    "billingEmail": "example@example.com",
    "createdTime": 1234567890
  },
  
  "saleEvent": null,
  
  "category": {
    "categoryId": 2,
    "name": "Awesome Products",
    "url": "https://shoplately.com/category/awesome-products",
    "parent": {
      "categoryId": 1,
      "name": "All Products",
      "url": "https://shoplately.com",
      "parent": null
    }
  },
  
  "options": [
    {
      "optionId": 104,
      "name": "Small/Blue",
      "sku": "MY-OWN-SKU-1",
      "quantity": 20,
      "sold": 0,
      "isSoldOut": false,
      "createdTime": 1234567890,
      "soldOutTime": null,
      "details": [
        {
          "optionDetailId": 108,
          "type": "Size",
          "name": "Small"
        },
        {
          "optionDetailId": 109,
          "type": "Color",
          "name": "Blue"
        }
      ],
      "images": [
        "https://shoplately.com/images/product/3/option/104/1.jpg",
        "https://shoplately.com/images/product/3/option/104/2.jpg"
      ]
    },
    {
      "optionId": 105,
      "name": "Large/Blue",
      "sku": "MY-OWN-SKU-2",
      "quantity": 20,
      "sold": 0,
      "isSoldOut": false,
      "createdTime": 1234567890,
      "soldOutTime": null,
      "details": [
        {
          "optionDetailId": 110,
          "type": "Size",
          "name": "Large"
        },
        {
          "optionDetailId": 111,
          "type": "Color",
          "name": "Blue"
        }
      ],
      "images": [
        "https://shoplately.com/images/product/3/option/105/1.jpg",
        "https://shoplately.com/images/product/3/option/105/2.jpg"
      ]
    },
  ]
}
```

This endpoint facilitates the creation of a new product.

The `Company` is automatically set based on the company associated with the user's API key.

### HTTP Request

`POST /api/v1/products`

### Payload
Name | Type | Description
---- | ---- | -----------
name | string | Product name
description | string | Product description
material | string | Product material description
measurement | string | Product measurement description
saleEventId | int | Existing sale event ID
categoryId | int | Existing category ID
regularPrice | float | Regular price
salePrice | float | Discounted on-sale price
optionDetail2Type | string | Second option detail type
options | array | (See below.)

### Option Object
Name | Type | Description
---- | ---- | -----------
name | string | Option name
sku | string | SKU of option
quantity | int | Available quantity of this option
details | object | Map of option detail types to option detail names. Must be "Size" and the type specified in "optionDetail2Type".
images | array | Absolute image URLs


## Update Product Info

This endpoint facilitates the updating of product information.

<aside class="notice">"Note": Quantities are associated with options as opposed to the products themselves. 
See <a href="#update-product-quantity">Update Product Quantity</a> for more information.</aside>

### HTTP Request

`PUT /api/v1/products/<productId>`

### URL Parameters
Name | Type | Description
---- | ---- | -----------
productId | int | Product ID

### Payload
Name | Type | Description
---- | ---- | -----------
name | string | Product name
description | string | Product description
material | string | Product material description
measurement | string | Product measurement description
saleEventId | int | Existing sale event ID
categoryId | int | Existing category ID
regularPrice | float | Regular price
salePrice | float | Discounted on-sale price


## Update Product Quantity <a name="update-product-quantity"></a>

### HTTP Request

`PUT /api/v1/options/<optionId>`

### URL Parameters
Name | Type | Description
---- | ---- | -----------
optionId | int | Option ID

### Payload
Name | Type | Description
---- | ---- | -----------
quantity | int | Available quantity of this option

## Out of stock

This endpoint changes the quantity of a product to 0 (including all options).

### HTTP Request

`DELETE /api/v1/products/<productId>/stock`

