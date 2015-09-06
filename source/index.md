---
title: API Reference

language_tabs:
  - shell

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - product
  - order
  - order_status
  - category
  - customer_service
  - errors

search: true
---

# Introduction

[Shoplately](http://shoplately.com) API documentation

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow"
```

> Make sure to replace `meowmeowmeow` with your API key.

Shoplately expects for the API key to be included in all API requests to the server in a header that looks like the following:

`X-SHOPLATELY-API-KEY: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>







