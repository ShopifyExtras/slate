---
title: Zapiet PUDO API Reference

language_tabs:
  - shell: cURL
  - php: PHP

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://apps.shopify.com/click-and-collect'>Start 14 day free trial of Zapiet now!</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Zapiet PUDO API. You can use this API to integrate your PUDO (pickup/dropoff) services directly into our platform.

We have language bindings in Shell and PHP. You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

# Authentication

> To authorize, use this code:

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

# Accounts 

## Get Accounts
Receive a list of all Accounts which have your services installed.

### HTTP Request
`GET https://api.zapiet.com/v2.0/services/accounts`

## Get Account
Receive a single Account.

### HTTP Request
`GET https://api.zapiet.com/v2.0/services/accounts/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Account to retrieve

## Activate
Activates your services on the specific Account.

### HTTP Request
`POST https://api.zapiet.com/v2.0/services/accounts/#{id}/activate`

### Query Parameters

Parameter | Description
--------- | -----------
id | The ID of the Account you wish to activate your services on

## Deactivate
Deactivates your service on a specific Account.

### HTTP Request
`POST https://api.zapiet.com/v2.0/services/accounts/#{id}/deactivate`

### Query Parameters

Parameter | Description
--------- | -----------
account_id | The ID of the Account account you wish to remove your services from

# Locations 

## Get Locations
Receive a list of all your Locations you've added to Zapiet.

### HTTP Request
`GET https://api.zapiet.com/v2.0/services/locations`

## Get Location
Receive a specific Location you have added to Zapiet.

### HTTP Request
`GET https://api.zapiet.com/v2.0/services/locations/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Location to retrieve

## Create Location
Creates a new Location within Zapiet.

### HTTP Request
`POST https://api.zapiet.com/v2.0/services/locations`

## Update Location 
Updates an existing Location within Zapiet.

### HTTP Request
`PUT https://api.zapiet.com/v2.0/services/locations/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Location to update

## Delete Location
Delete an existing Location.

`DELETE https://api.zapiet.com/v2.0/services/locations/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Location to delete

# Orders

## Get Orders
Receive all Orders.

### HTTP Request
`GET https://api.zapiet.com/v2.0/services/orders`

Parameter | Default | Description
--------- | ------- | -----------
limit | 50 | Amount of results to return, maximum 250
page | 1 | Page to show
last_order_id | | Restrict results to after the specified ID
status | open | open - All open orders<br>closed - Show only closed orders<br>cancelled - Show only cancelled orders<br>any - Any order status

## Get Order
Receive a specific Order.

### HTTP Request
`GET https://api.zapiet.com/v2.0/services/orders/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Order to retrieve

## Update Order
Updates an existing Order.

### HTTP Request
`PUT https://api.zapiet.com/v2.0/services/orders/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Order to update

# Webhooks

## Get Webhooks
Receive a list of all Webhooks.

### HTTP Request
`GET https://api.zapiet.com/v2.0/services/webhooks`

## Get Webhook
Receive a specific Webhook.

### HTTP Request
`GET https://api.zapiet.com/v2.0/services/webhooks/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Webook to retrieve

## Create Webhook
Creates a new Webhook.

### HTTP Request
`POST https://api.zapiet.com/v2.0/services/webhooks`

## Update Webhook
Updates an existing Webhook.

### HTTP Request
`PUT https://api.zapiet.com/v2.0/services/webhooks/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Webhook to update

## Delete Webhook
Delete an existing Webhook.

`DELETE https://api.zapiet.com/v2.0/services/webhooks/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Webhook to delete

# Kittens

## Get All Kittens

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">If you're not using an administrator API key, note that some kittens will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

