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
    "name": "All Products",
    "url": "https://shoplately.com",
    "children": [
        {
            "categoryId": 2,
            "name": "Awesome Products",
            "url": "https://shoplately.com/category/awesome-products",
            "children": [
            	{
                	"categoryId": 3,
                	"name": "Moderately Awesome Products",
                	"url": "https://shoplately.com/category/moderately-awesome-products",
                	"children": null
                },
                {
                	"categoryId": 4,
                	"name": "Super Awesome Products",
                	"url": "https://shoplately.com/category/super-awesome-products",
                	"children": null
                }
            ]
        },
        {
            "categoryId": 5,
            "name": "Example Products",
            "url": "https://shoplately.com/category/example-products",
            "children": null
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