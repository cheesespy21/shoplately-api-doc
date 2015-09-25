# Category

## Get All Categories

```shell
curl "http://api.lately.com/v1/categories" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
    "categoryId": 1,
    "name": "All",
    "url": "https://shoplately.com",
    "parentId": 0,
    "children": [
        {
            "categoryId": 18,
            "name": "Accessories",
            "url": "https://shoplately.com/shop/accessories",
            "parentId": 1,
            "children": [
                {
                    "categoryId": 20,
                    "name": "Bags",
                    "url": "https://shoplately.com/shop/bags",
                    "parentId": 18,
                    "children": [
                        {
                            "categoryId": 41,
                            "name": "Backpacks",
                            "url": "https://shoplately.com/shop/bags-backpacks",
                            "parentId": 20,
                            "children": []
                        },
                        {
                            "categoryId": 56,
                            "name": "Handbag Hangers",
                            "url": "https://shoplately.com/shop/bags-handbag-hangers",
                            "parentId": 20,
                            "children": []
                        }
                    ]
                }
            ]
        }
    ]
}
```

This endpoint retrieves a full category tree.

<aside class="notice">Note: The <strong>parent</strong> attribute is replaced with a <strong>children</strong> attribute in objects returned by this endpoint in order to best represent the category hierarchy .</aside>

### HTTP Request

`GET /v1/categories`

### Query Parameters
Parameter | Default | Description
--------- | ------- | -----------
depth | 10 | Maximum number of child categories to traverse from the root level

### Returns
This endpoint returns an array of Category objects.