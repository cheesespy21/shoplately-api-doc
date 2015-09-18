# Customer Service

## Get Inbox

```shell
curl "https://shoplately.com/api/v1/messages" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
	{
		"threadId": 100,
		"to": {
			"details": {
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
            "isCompany": true,
			"isAdmin": false
        },
        "from": {
			"details": {
            	"userId": 100,
            	"name": "Henry Jekyll",
            	"image": null,
            	"createdTime": 1234567890
        	},
            "isCompany": false,
            "isAdmin": false
        },
        "subject": "Question about order",
        "purchase": { ... },
        "messages": [
        	{
            	"messageId": 101,
                "author": {
                	"details": {
            			"userId": 100,
            			"name": "Henry Jekyll",
            			"image": null,
            			"createdTime": 1234567890
        			},
            		"isCompany": false,
            		"isAdmin": false
                },
                "message": "Hiya! When will my order be shipping?",
                "createdTime": 1234567890
            },
            {
            	"messageId": 102,
                "author": {
                	"details": {
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
            		"isCompany": true,
					"isAdmin": false
                },
                "message": "Hi Henry, due to an inventory issue, this order will be shipped next week. Thanks for understanding.",
                "createdTime": 1234567890
            }
        ],
        "createdTime": 1234567890
    },

	{
		"threadId": 200,
		"to": {
        	"details": {
            	"userId": 100,
            	"name": "Henry Jekyll",
            	"image": null,
            	"createdTime": 1234567890
        	},
            "isCompany": false,
            "isAdmin": false
        },
        "from": {
			"details": {
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
            "isCompany": true,
			"isAdmin": false
        },
        "subject": "Order update",
        "purchase": { ... },
        "messages": [
        	{
            	"messageId": 201,
                "author": {
                	"details": {
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
                    "isCompany": true,
					"isAdmin": false
                },
                "message": "Hi Henry, this message is to let you know that your order has been shipped.",
                "createdTime": 1234567890
            }
        ],
        "createdTime": 1234567890
    }
]
```

### HTTP Request

`GET /api/v1/messages`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page | 1 | Page number
limit | 25 | The number of products to be retrieved

## Create Thread

```shell
curl -XPOST "https://shoplately.com/api/v1/messages" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow"
  -d '{
    "toUserId": 100,
    "subject": "Test message",
    "purchaseId": 100,
    "message": "This is a test message!"
  }'
```

> The above command returns the entire thread in JSON format.

This endpoint allows a company to create a thread to a user.

### HTTP Request

`POST /api/v1/messages`

### Payload
Name | Type | Description
---- | ---- | -----------
toUserId | int | Recipient user ID
subject | string | Message subject
purchaseId | int | Purchase ID
message | string | Message body


## Respond to Thread

```shell
curl -XPOST "https://shoplately.com/api/v1/messages/100" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow"
  -d '{
    "message": "This is a reply!"
  }'
```

> The above command returns the entire thread in JSON format.

This endpoint allows a company to reply to a thread.

### HTTP Request

`POST /api/v1/messages/<threadId>`

### URL Parameters
Name | Type | Description
---- | ---- | -----------
threadId | int | Thread ID

### Payload
Name | Type | Description
---- | ---- | -----------
message | string | Message body