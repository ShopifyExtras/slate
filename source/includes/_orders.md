# Orders

## Get Orders
Receive all Orders.

### HTTP Request
`GET /services/orders`

Parameter | Default | Description
--------- | ------- | -----------
limit | 50 | Amount of results to return, maximum 250
page | 1 | Page to show
last_order_id | | Restrict results to after the specified ID
status | open | open - All open orders<br>closed - Show only closed orders<br>cancelled - Show only cancelled orders<br>any - Any order status

## Get Order
Receive a specific Order.

### HTTP Request
`GET /services/orders/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Order to retrieve

## Update Order
Updates an existing Order.

### HTTP Request
`PUT /services/orders/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Order to update